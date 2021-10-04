# django password help_text

~~~
from django.utils.safestring import mark_safe


helper = """
<ul>
<li>Şifreniz diğer bilgilerinize benzer olamaz.</li>
<li>Şifreniz en az 8 karakter içermeli.</li>
<li>Şifreniz çok bilindik şifrelerden olmamalı.</li>
<li>Şifreniz tamamen rakamlardan oluşamaz.</li>
</ul>
"""

email = forms.EmailField(label="E-mail adresiniz")
password1 = forms.CharField(
    label="Şifreniz",
    widget=forms.PasswordInput,
    help_text=mark_safe(helper),
)
password2 = forms.CharField(label="Şifrenizin tekrarı", widget=forms.PasswordInput)
~~~
