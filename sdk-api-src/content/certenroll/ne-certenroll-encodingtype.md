---
UID: NE:certenroll.EncodingType
title: EncodingType
author: windows-sdk-content
description: Specifies the type of encoding applied to a byte array for display purposes.
old-location: security\encodingtype_enum.htm
old-project: SecCertEnroll
ms.assetid: b42628ae-deed-497b-a20f-d175843b79c2
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EncodingType, EncodingType enumeration [Security], XCN_CRYPT_STRING_ANY, XCN_CRYPT_STRING_BASE64, XCN_CRYPT_STRING_BASE64HEADER, XCN_CRYPT_STRING_BASE64REQUESTHEADER, XCN_CRYPT_STRING_BASE64X509CRLHEADER, XCN_CRYPT_STRING_BASE64_ANY, XCN_CRYPT_STRING_BINARY, XCN_CRYPT_STRING_HEX, XCN_CRYPT_STRING_HEXADDR, XCN_CRYPT_STRING_HEXASCII, XCN_CRYPT_STRING_HEXASCIIADDR, XCN_CRYPT_STRING_HEXRAW, XCN_CRYPT_STRING_HEX_ANY, XCN_CRYPT_STRING_NOCR, XCN_CRYPT_STRING_NOCRLF, certenroll/EncodingType, certenroll/XCN_CRYPT_STRING_ANY, certenroll/XCN_CRYPT_STRING_BASE64, certenroll/XCN_CRYPT_STRING_BASE64HEADER, certenroll/XCN_CRYPT_STRING_BASE64REQUESTHEADER, certenroll/XCN_CRYPT_STRING_BASE64X509CRLHEADER, certenroll/XCN_CRYPT_STRING_BASE64_ANY, certenroll/XCN_CRYPT_STRING_BINARY, certenroll/XCN_CRYPT_STRING_HEX, certenroll/XCN_CRYPT_STRING_HEXADDR, certenroll/XCN_CRYPT_STRING_HEXASCII, certenroll/XCN_CRYPT_STRING_HEXASCIIADDR, certenroll/XCN_CRYPT_STRING_HEXRAW, certenroll/XCN_CRYPT_STRING_HEX_ANY, certenroll/XCN_CRYPT_STRING_NOCR, certenroll/XCN_CRYPT_STRING_NOCRLF, security.encodingtype_enum
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EncodingType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - EncodingType
product: Windows
targetos: Windows
req.lib: Certidl.lib
req.dll: Certenc.dll
req.irql: 
---

# EncodingType enumeration


## -description


The <b>EncodingType</b> enumeration specifies the type of encoding applied to a byte array for display purposes.


## -enum-fields




### -field XCN_CRYPT_STRING_BASE64HEADER

The string is base64 encoded with beginning and ending certificate headers. Base64 is an encoding scheme  used to transmit binary data. The data to be encoded is examined three bytes at a time. Every six bits in the 24-bit buffer is used as an index into a text string. The strings used vary depending on the type of data being encoded. The following string is commonly used for Multipurpose Internet Mail Extensions (MIME) email base64 encoding.

<pre class="syntax" xml:space="preserve"><code>ABCDEFGHIJKLMNOPQRSTUVWXYZabcdefghijklmnopqrstuvwxyz0123456789+/</code></pre>
 The following example shows a certificate that is base64 encoded and includes the beginning and ending headers.

<pre class="syntax" xml:space="preserve"><code>-----BEGIN CERTIFICATE-----
MIIBqDCCARECAQAwaTELMAkGA1UEBhMCVVMxDjAMBgNVBAgTBVRleGFzMRMwEQYD
VQQHEwpMYXNDb2xpbmFzMRIwEAYDVQQKEwlNaWNyb3NvZnQxDjAMBgNVBAsTBUl0
ZWFtMREwDwYDVQQDFAhOVFZPT0RPTzCBnjANBgkqhkiG9w0BAQEFAAOBjAAwgYgC
gYBxmmAWKbLJHg5TuVyjgzWW0JsY5Shaqd7BDWtqhzy4HfRTW22f31rlm8NeSXHn
EhLiwsGgNzWHJ8no1QIYzAgpDR79oqxvgrY4WS3PXT7OLwIDAQABoAAwDQYJKoZI
hvcNAQEEBQADgYEAVcyI4jtnnV6kMiByiq4Xg99yL0U7bIpEwAf3MIZHS7wuNqfY
acfhbRj6VFHT8ObprKGPmqXJvwrBmPrEuCs4Ik6PidAAeEfoaa3naIbM73tTvKN+
WD30lAfGBr8SZixLep4pMIN/wO0eu6f30cBuoPtDnDulNT8AuQHjkJIc8Qc=
-----END CERTIFICATE----- </code></pre>

### -field XCN_CRYPT_STRING_BASE64

The string is base64 encoded without beginning and ending certificate headers.


### -field XCN_CRYPT_STRING_BINARY

The string is a pure binary sequence. It is not encoded.


### -field XCN_CRYPT_STRING_BASE64REQUESTHEADER

The string is base64 encoded with beginning and ending certificate request headers. This is shown in the following example.

<pre class="syntax" xml:space="preserve"><code>-----BEGIN NEW CERTIFICATE REQUEST-----
MIIDBjCCAm8CAQAwcTERMA8GA1UEAxMIcXV1eC5jb20xDzANBgNVBAsTBkJyYWlu
czEWMBQGA1UEChMNRGV2ZWxvcE1lbnRvcjERMA8GA1UEBxMIVG9ycmFuY2UxEzAR
BgNVBAgTCkNhbGlmb3JuaWExCzAJBgNVBAYTAlVTMIGfMA0GCSqGSIb3DQEBAQUA
A4GNADCBiQKBgQDFUxFtzr170yxptKuGI1590Sta5z2dVElLfjAn+q4T1uZE3DiH
HXNRHW1eS9W2aeMZhRnYRi5U8eOdG3RUO4YXy4B1sqfy5I0qjjySA89ghVd/6JcA
K1nhGJL9FPJ6XKVUNLez7NpSCFlYs5foyTqyxDkHzTnQwRwkkwQ9dlbnfwIDAQAB
oIIBUzAaBgorBgEEAYI3DQIDMQwWCjUuMC4yMTk1LjIwNQYKKwYBBAGCNwIBDjEn
MCUwDgYDVR0PAQH/BAQDAgTwMBMGA1UdJQQMMAoGCCsGAQUFBwMBMIH9BgorBgEE
AYI3DQICMYHuMIHrAgEBHloATQBpAGMAcgBvAHMAbwBmAHQAIABSAFMAQQAgAFMA
QwBoAGEAbgBuAGUAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIA
bwB2AGkAZABlAHIDgYkAXxNuAz6gcBaZUdef8WQ2PAroKMW8sprcKv7QD2encz6/
Wct9DZ5CkGynLGy0f+Lff7ViSDJqxYWaJ68ddqgXyAqIilF63kivPTiC6yxLaNX6
5v3cnKFx4UrUrGXZtub7M7/NuxSipOW0Vv7yCHganypxDyRzp6IhulEnL4APEH4A
AAAAAAAAADANBgkqhkiG9w0BAQUFAAOBgQBljJb1ZhWOwOLfzfHbC3yxGkXDy9w3
NA7uhQOvgntnqmSmdHP9nsM3DnxwaHb3EVxMKbAuLsSRDAE1KGqeamvQ3uFjuuL0
5q4nKhX25LyGFDSc6h1OHcv+0ugZ/9klsiViSeEGpMwllUf057o7q1Vls4HN22vM
wkcejcttDjo3Kw==
-----END NEW CERTIFICATE REQUEST-----</code></pre>

### -field XCN_CRYPT_STRING_HEX

The string is hexadecimal encoded. Each 4-bit nibble of the string is represented as a number between zero and nine or a letter between A and F (or a and f). This is shown in the following example.

<pre class="syntax" xml:space="preserve"><code>3a 20 63 65 72 74 6c 69  62 5c 6c 64 61 70 2e 63
70 70 28 32 31 33 31 29  3a 20 6c 64 61 70 65 72
...</code></pre>

### -field XCN_CRYPT_STRING_HEXASCII

The string is hexadecimal encoded, and the corresponding ASCII characters are displayed. This is shown in the following example.

<pre class="syntax" xml:space="preserve"><code>3a 20 63 65 72 74 6c 69  62 5c 6c 64 61 70 2e 63   : certlib\ldap.c
70 70 28 32 31 33 31 29  3a 20 6c 64 61 70 65 72   pp(2131): ldaper
...</code></pre>

### -field XCN_CRYPT_STRING_BASE64_ANY

The string is base64 encoded. Enumeration values are tried in the following order:

<ol>
<li><b>XCN_CRYPT_STRING_BASE64HEADER</b></li>
<li><b>XCN_CRYPT_STRING_BASE64</b></li>
</ol>

### -field XCN_CRYPT_STRING_ANY

Enumeration values are tried in the following order:

<ol>
<li><b>XCN_CRYPT_STRING_BASE64_ANY</b></li>
<li><b>XCN_CRYPT_STRING_BINARY</b></li>
</ol>
The <b>XCN_CRYPT_STRING_BINARY</b> value always succeeds.


### -field XCN_CRYPT_STRING_HEX_ANY

Enumeration values are tried in the following order:

<ol>
<li><b>XCN_CRYPT_STRING_HEXADDR</b></li>
<li><b>XCN_CRYPT_STRING_HEXASCIIADDR</b></li>
<li><b>XCN_CRYPT_STRING_HEXASCII</b></li>
<li><b>XCN_CRYPT_STRING_HEX</b></li>
</ol>

### -field XCN_CRYPT_STRING_BASE64X509CRLHEADER

The string is base64 encoded with beginning and ending <a href="https://msdn.microsoft.com/28dba6ef-939f-4789-9789-ee6e0fef0177">X.509</a> <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) headers. This is shown in the following example.

<pre class="syntax" xml:space="preserve"><code>-----BEGIN X509 CRL-----
MIIDBjCCAm8CAQAwcTERMA8GA1UEAxMIcXV1eC5jb20xDzANBgNVBAsTBkJyYWlu
czEWMBQGA1UEChMNRGV2ZWxvcE1lbnRvcjERMA8GA1UEBxMIVG9ycmFuY2UxEzAR
BgNVBAgTCkNhbGlmb3JuaWExCzAJBgNVBAYTAlVTMIGfMA0GCSqGSIb3DQEBAQUA
A4GNADCBiQKBgQDFUxFtzr170yxptKuGI1590Sta5z2dVElLfjAn+q4T1uZE3DiH
HXNRHW1eS9W2aeMZhRnYRi5U8eOdG3RUO4YXy4B1sqfy5I0qjjySA89ghVd/6JcA
K1nhGJL9FPJ6XKVUNLez7NpSCFlYs5foyTqyxDkHzTnQwRwkkwQ9dlbnfwIDAQAB
oIIBUzAaBgorBgEEAYI3DQIDMQwWCjUuMC4yMTk1LjIwNQYKKwYBBAGCNwIBDjEn
MCUwDgYDVR0PAQH/BAQDAgTwMBMGA1UdJQQMMAoGCCsGAQUFBwMBMIH9BgorBgEE
AYI3DQICMYHuMIHrAgEBHloATQBpAGMAcgBvAHMAbwBmAHQAIABSAFMAQQAgAFMA
QwBoAGEAbgBuAGUAbAAgAEMAcgB5AHAAdABvAGcAcgBhAHAAaABpAGMAIABQAHIA
bwB2AGkAZABlAHIDgYkAXxNuAz6gcBaZUdef8WQ2PAroKMW8sprcKv7QD2encz6/
Wct9DZ5CkGynLGy0f+Lff7ViSDJqxYWaJ68ddqgXyAqIilF63kivPTiC6yxLaNX6
5v3cnKFx4UrUrGXZtub7M7/NuxSipOW0Vv7yCHganypxDyRzp6IhulEnL4APEH4A
AAAAAAAAADANBgkqhkiG9w0BAQUFAAOBgQBljJb1ZhWOwOLfzfHbC3yxGkXDy9w3
NA7uhQOvgntnqmSmdHP9nsM3DnxwaHb3EVxMKbAuLsSRDAE1KGqeamvQ3uFjuuL0
5q4nKhX25LyGFDSc6h1OHcv+0ugZ/9klsiViSeEGpMwllUf057o7q1Vls4HN22vM
wkcejcttDjo3Kw==
-----END X509 CRL-----</code></pre>

### -field XCN_CRYPT_STRING_HEXADDR

The string is hexadecimal encoded and displayed as a hexadecimal address. This is shown in the following example.

<pre class="syntax" xml:space="preserve"><code>0000  3a 20 63 65 72 74 6c 69  62 5c 6c 64 61 70 2e 63
0010  70 70 28 32 31 33 31 29  3a 20 6c 64 61 70 65 72
...</code></pre>

### -field XCN_CRYPT_STRING_HEXASCIIADDR

The string is hexadecimal encoded and displayed as a hexadecimal address along with the corresponding ASCII characters. This is shown in the following example.

<pre class="syntax" xml:space="preserve"><code>0000  3a 20 63 65 72 74 6c 69  62 5c 6c 64 61 70 2e 63   : certlib\ldap.c
0010  70 70 28 32 31 33 31 29  3a 20 6c 64 61 70 65 72   pp(2131): ldaper
...</code></pre>

### -field XCN_CRYPT_STRING_HEXRAW

The string is hexadecimal encoded and displayed without punctuation. <b>XCN_CRYPT_STRING_HEXRAW</b> is available only with Windows Vista.

<pre class="syntax" xml:space="preserve"><code>3a20636572746c69625c6c6461702e6370702832313331293a206c6461706572...</code></pre>

### -field XCN_CRYPT_STRING_BASE64URI


### -field XCN_CRYPT_STRING_ENCODEMASK


### -field XCN_CRYPT_STRING_CHAIN


### -field XCN_CRYPT_STRING_TEXT


### -field XCN_CRYPT_STRING_PERCENTESCAPE


### -field XCN_CRYPT_STRING_HASHDATA


### -field XCN_CRYPT_STRING_STRICT


### -field XCN_CRYPT_STRING_NOCRLF

Removes carriage return and line feed control characters from the encoded string.


### -field XCN_CRYPT_STRING_NOCR

Removes the carriage return control character from the encoded string.


## -see-also




<a href="https://msdn.microsoft.com/8514fb89-1cf5-4e09-997c-17984efc4e03">CertEnroll Enumerations</a>



<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>
 

 

