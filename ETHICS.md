# Programmer Code of Ethics

## Preamble

Programmers thrive by solving interesting challenges. Many programmers work on
behalf of others - a company, a government, etc. Sometimes the programmer will
work for a corrupt employer. Often, they will be asked to write unethical
software. Someone wrote xkeyscore. Someone wrote superfish. We need to establish
a code of ethics, as programmers, to ensure that we don't let our desire to
solve interesting and difficult problems drive us to write software that has a
negative impact on the world. This document is the means by which we commit to
writing ethical software.

Those in the signatures directory have pledged themselves to write ethical
software. This document defines the values that they uphold by doing so. You,
programmer, are encouraged to review this document and consider signing it
yourself. See
"[SIGNING.md](https://github.com/SirCmpwn/ethics/blob/master/SIGNING.md)" for
instructions on how to do so. You, employer, are encouraged to review this
document and refrain from asking your developers to write software that
violates its guidelines.

Software developers are in extremely high demand. You have the power to say
"no." You have the power to walk away from an unethical job. Exercise it.

### Scope

There are many practices that are questionably ethical, such as bundling adware
in software installers. This document does not attempt to address all of these
scenarios. Instead, it addresses only the most severe problems that are
relevant to our profession today.

## Unethical Practices

I, the programmer or company, agree that I will refuse to knowingly write any
software that uses these practices.

### Security theater

This refers to software that carries the implication of security while in fact
being insecure. Examples include:

#### Broken or insecure cryptographic algorithms

Cryptography changes over time, and weaknesses or flaws are found in some
algorithms. Do not write software that knowingly uses flawed algorithms - on all
projects, research the strongest algorithms of the current day and use only
those. Never compromise on your choice of algorithms.

Use of less powerful cryptographic algorithms is permitted when circumstances
force your hand, but only when adequately disclosed. For example, embedded
systems may not have the capability to use sophisticated encryption algorithms
performantly. If you must downgrade your cryptography, you **must** clearly
disclose this fact to your users.

#### Fundamental platform flaws

Do not write software that claims to be secure but is fundamentally flawed by
the platform it runs on. For example, using cryptography with Javascript in a
web browser is not effective because the distribution mechanism (your web
server) can be easily compromised and serve alternate Javascript without
notifying the user of the change.

### Subverting user security

Do not intentionally subvert applications that provide security for your users.
Do not write software that compromises other software installed on the same
machine. An example of failing to uphold this is the Superfish malware, which
installed a new root certificate on user's computers to enable man-in-the-middle
attacks that compromised the security of the user's TLS sessions. If it's
encrypted, it's none of your business.

### Unnecessary data collection

Do not write software that collects personal information about users without
their knowledge and consent. Anonymizing and aggregating user information for
broader analysis is acceptable. If you will collect any personal information
about a user, you **must** disclose exactly what data you are collecting. You
**must** allow users to purge the data you have collected about them.

The above guidelines do not apply if you are a member of a government *and have
obtained a warrant* with respect to your laws.

You may not exchange any collected personal information with other parties.

When collecting information, even with disclosure, you must have a specific
use-case to justify the need for the data you are collecting. You, the
programmer, should judge for yourself whether or not the data you are collecting
is necessary and ethical to collect.

### Open source license subversion

Abide by the terms set forth in the licenses of open source software you depend
on. It's your responsibility as a programmer, when introducing dependencies, to
review the license and ensure that the stakeholders of your project are aware of
the implications, and to follow through with them. Do not resort to obfuscation
to hide your license violations - do not make violations in the first place.
