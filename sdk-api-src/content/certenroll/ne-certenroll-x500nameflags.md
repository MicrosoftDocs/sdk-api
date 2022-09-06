---
UID: NE:certenroll.X500NameFlags
title: X500NameFlags (certenroll.h)
description: Specifies the display and encoding characteristics of a distinguished name or relative distinguished name (RDN).
helpviewer_keywords: ["X500NameFlags","X500NameFlags enumeration [Security]","XCN_CERT_NAME_STR_COMMA_FLAG","XCN_CERT_NAME_STR_CRLF_FLAG","XCN_CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG","XCN_CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG","XCN_CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG","XCN_CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG","XCN_CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG","XCN_CERT_NAME_STR_FORWARD_FLAG","XCN_CERT_NAME_STR_NONE","XCN_CERT_NAME_STR_NO_PLUS_FLAG","XCN_CERT_NAME_STR_NO_QUOTING_FLAG","XCN_CERT_NAME_STR_REVERSE_FLAG","XCN_CERT_NAME_STR_SEMICOLON_FLAG","XCN_CERT_OID_NAME_STR","XCN_CERT_SIMPLE_NAME_STR","XCN_CERT_X500_NAME_STR","XCN_CERT_XML_NAME_STR","certenroll/X500NameFlags","certenroll/XCN_CERT_NAME_STR_COMMA_FLAG","certenroll/XCN_CERT_NAME_STR_CRLF_FLAG","certenroll/XCN_CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG","certenroll/XCN_CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG","certenroll/XCN_CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG","certenroll/XCN_CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG","certenroll/XCN_CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG","certenroll/XCN_CERT_NAME_STR_FORWARD_FLAG","certenroll/XCN_CERT_NAME_STR_NONE","certenroll/XCN_CERT_NAME_STR_NO_PLUS_FLAG","certenroll/XCN_CERT_NAME_STR_NO_QUOTING_FLAG","certenroll/XCN_CERT_NAME_STR_REVERSE_FLAG","certenroll/XCN_CERT_NAME_STR_SEMICOLON_FLAG","certenroll/XCN_CERT_OID_NAME_STR","certenroll/XCN_CERT_SIMPLE_NAME_STR","certenroll/XCN_CERT_X500_NAME_STR","certenroll/XCN_CERT_XML_NAME_STR","security.x500nameflags_enum"]
old-location: security\x500nameflags_enum.htm
tech.root: security
ms.assetid: 8961f21c-1aab-4bbf-a696-e5bc0f37724a
ms.date: 12/05/2018
ms.keywords: X500NameFlags, X500NameFlags enumeration [Security], XCN_CERT_NAME_STR_COMMA_FLAG, XCN_CERT_NAME_STR_CRLF_FLAG, XCN_CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG, XCN_CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG, XCN_CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG, XCN_CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG, XCN_CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG, XCN_CERT_NAME_STR_FORWARD_FLAG, XCN_CERT_NAME_STR_NONE, XCN_CERT_NAME_STR_NO_PLUS_FLAG, XCN_CERT_NAME_STR_NO_QUOTING_FLAG, XCN_CERT_NAME_STR_REVERSE_FLAG, XCN_CERT_NAME_STR_SEMICOLON_FLAG, XCN_CERT_OID_NAME_STR, XCN_CERT_SIMPLE_NAME_STR, XCN_CERT_X500_NAME_STR, XCN_CERT_XML_NAME_STR, certenroll/X500NameFlags, certenroll/XCN_CERT_NAME_STR_COMMA_FLAG, certenroll/XCN_CERT_NAME_STR_CRLF_FLAG, certenroll/XCN_CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG, certenroll/XCN_CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG, certenroll/XCN_CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG, certenroll/XCN_CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG, certenroll/XCN_CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG, certenroll/XCN_CERT_NAME_STR_FORWARD_FLAG, certenroll/XCN_CERT_NAME_STR_NONE, certenroll/XCN_CERT_NAME_STR_NO_PLUS_FLAG, certenroll/XCN_CERT_NAME_STR_NO_QUOTING_FLAG, certenroll/XCN_CERT_NAME_STR_REVERSE_FLAG, certenroll/XCN_CERT_NAME_STR_SEMICOLON_FLAG, certenroll/XCN_CERT_OID_NAME_STR, certenroll/XCN_CERT_SIMPLE_NAME_STR, certenroll/XCN_CERT_X500_NAME_STR, certenroll/XCN_CERT_XML_NAME_STR, security.x500nameflags_enum
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: X500NameFlags
req.redist: 
ms.custom: 19H1
f1_keywords:
 - X500NameFlags
 - certenroll/X500NameFlags
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - CertEnroll.h
api_name:
 - X500NameFlags
---

# X500NameFlags enumeration


## -description

The <b>X500NameFlags</b> enumeration type specifies the display and <a href="/windows/desktop/SecGloss/e-gly">encoding</a> characteristics of a distinguished name or <a href="/windows/desktop/SecGloss/r-gly">relative distinguished name</a> (RDN).  This enumeration is used to initialize an <a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a> object.

## -enum-fields

### -field XCN_CERT_NAME_STR_NONE:0

Display characteristics are not identified.

### -field XCN_CERT_SIMPLE_NAME_STR:1

All <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs) are discarded. <a href="/windows/desktop/SecGloss/r-gly">Relative distinguished names</a> (RDNs) are separated by commas followed by a space (, ). RDN attributes are separated by a plus sign enclosed within spaces ( + ).

### -field XCN_CERT_OID_NAME_STR:2

OIDs are separated from their associated attribute value by using an equal sign (=). RDNs are separated by a comma followed by a space (, ). RDN attributes are separated by a plus sign followed by a space (+ ).

### -field XCN_CERT_X500_NAME_STR:3

OIDs are converted to their <a href="/windows/desktop/SecGloss/x-gly">X.500</a> key names. They are separated from their associated attribute value by using an equal sign (=). RDNs are separated by a comma followed by a space (, ). RDN attributes are separated by a plus sign followed by a space (+ ).

If an OID does not have a corresponding X.500 name, the OID is used with a prefix of OID. The RDN is enclosed within quotation marks (" ") if it contains leading or trailing white space or one of the following characters:<ul>
<li>Comma (,)</li>
<li>Plus sign (+)</li>
<li>Equal sign (=)</li>
<li>Inch mark (")</li>
<li>Line feed (\n)</li>
<li>Less than sign (&lt;)</li>
<li>Greater than sign (&gt;)</li>
<li>Number sign (#)</li>
<li>Semicolon (;)</li>
<li>Embedded quotation mark (")</li>
</ul>

### -field XCN_CERT_XML_NAME_STR:4

OIDs are treated in the same manner as that used to convert XCN_CERT_X500_NAME_ST values except that they are formatted as a sequence of XML elements. This is shown in the following example.


``` syntax

&lt;CN&gt;cart.contoso.com&lt;/CN&gt;
&lt;OU&gt;Terms of use at www.verisign.com/rpa (c)00&lt;/OU&gt;
&lt;OU rDNAttribute="true"&gt;IT Operations&lt;/OU&gt;
&lt;O&gt;Contoso.com&lt;/O&gt;
&lt;L&gt;New York&lt;/L&gt;
&lt;S&gt;New York&lt;/S&gt;
&lt;C&gt;US&lt;/C&gt;
&lt;RDN oid="1.2.3.4" type="string"&gt;name&lt;/RDN&gt;
&lt;RDN rDNAttribute="true" oid="1.2.1.3" type="encoded"&gt;0500&lt;/RDN&gt;
&lt;RDN oid="1.2.1.4" type="encoded"&gt;020135&lt;/RDN&gt;
&lt;RDN oid="1.2.2.5.3" type="octet"&gt;01FF7F&lt;/RDN&gt;
```

The Unicode XML markup characters are escaped in the following manner. Characters greater than 0x7F are escaped by using character references (L"&amp;#xXXXX;").
<ul>
<li>&amp; becomes L"&amp;amp;"</li>
<li>&lt; becomes L"&amp;lt;"</li>
<li>&gt; becomes L"&amp;gt;"</li>
<li>\' becomes L"&amp;apos;"</li>
<li>\" becomes L"&amp;quot;"</li>
</ul>

### -field XCN_CERT_NAME_STR_SEMICOLON_FLAG:0x40000000

The comma (,) separator used between RDNs is replaced with a semicolon (;) character.

### -field XCN_CERT_NAME_STR_NO_PLUS_FLAG:0x20000000

The (+) separator used between RDN attributes is replaced with a single space character.

### -field XCN_CERT_NAME_STR_NO_QUOTING_FLAG:0x10000000

Inhibits the use of quotation marks for the XCN_CERT_X500_NAME_ST value.

### -field XCN_CERT_NAME_STR_CRLF_FLAG:0x8000000

The comma (,) separator used between RDNs is replaced with a carriage return/line feed (\r\n) sequence.

### -field XCN_CERT_NAME_STR_COMMA_FLAG:0x4000000

Specifies that the separator between RDNs is a comma (,).

### -field XCN_CERT_NAME_STR_REVERSE_FLAG:0x2000000

Specifies that the order of the RDNs that make up the distinguished name (DN) is reversed for encoding. The typical DN display order is CN=<i>name</i>,...,DC=<i>com</i>. Use this flag to change the encoding order to DC=<i>com</i>,...,CN=<i>name</i>. An <a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a> object sets this flag by default unless you specify  XCN_CERT_NAME_STR_FORWARD_FLAG.

### -field XCN_CERT_NAME_STR_FORWARD_FLAG:0x1000000

Use to undo the encoding order specified by setting the XCN_CERT_NAME_STR_REVERSE_FLAG value.

### -field XCN_CERT_NAME_STR_AMBIGUOUS_SEPARATOR_FLAGS

### -field XCN_CERT_NAME_STR_DISABLE_IE4_UTF8_FLAG:0x10000

Skips the initial attempt to decode T.61 Teletex character values to UTF-8 values. By default, T.61 values are initially decoded to UTF-8, but if UTF-8 decoding fails, the values are decoded as 8-bit characters.

### -field XCN_CERT_NAME_STR_ENABLE_T61_UNICODE_FLAG:0x20000

T.61 is used rather than Unicode character encoding for all characters less than 0xFF. LDAP, for example, uses T.61.

### -field XCN_CERT_NAME_STR_ENABLE_UTF8_UNICODE_FLAG:0x40000

UTF-8 is used for the DN instead of Unicode character encoding.

### -field XCN_CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG:0x80000

Forces the following X.500 keys to be encoded as UTF-8 strings rather than printable Unicode strings.

<table>
<tr>
<th>Key</th>
<th>OID</th>
</tr>
<tr>
<td>CN</td>
<td>XCN_OID_COMMON_NAME</td>
</tr>
<tr>
<td>G </td>
<td>XCN_OID_GIVEN_NAME</td>
</tr>
<tr>
<td>GivenName</td>
<td>XCN_OID_GIVEN_NAME</td>
</tr>
<tr>
<td>GN</td>
<td>XCN_OID_GIVEN_NAME</td>
</tr>
<tr>
<td>I</td>
<td>XCN_OID_INITIALS</td>
</tr>
<tr>
<td>Initials</td>
<td>XCN_OID_INITIALS</td>
</tr>
<tr>
<td>L</td>
<td>XCN_OID_LOCALITY_NAME</td>
</tr>
<tr>
<td>O</td>
<td>XCN_ORGANIZATION_NAME</td>
</tr>
<tr>
<td>OU </td>
<td>XCN_OID_ORGANIZATIONAL_UNIT_NAME</td>
</tr>
<tr>
<td>S</td>
<td>XCN_OID_STATE_OR_PROVINCE_NAME</td>
</tr>
<tr>
<td>SN</td>
<td>XCN_ID_SUR_NAME</td>
</tr>
<tr>
<td>ST</td>
<td>XCN_OID_STATE_OR_PROVINCE_NAME</td>
</tr>
<tr>
<td>STREET</td>
<td>XCN_OID_STREET_ADDRESS</td>
</tr>
<tr>
<td>T</td>
<td>XCN_OID_TITLE</td>
</tr>
<tr>
<td>Title</td>
<td>XCN_OID_TITLE</td>
</tr>
</table>

### -field XCN_CERT_NAME_STR_DISABLE_UTF8_DIR_STR_FLAG:0x100000

Prevents forcing printable Unicode strings to be encoded by using UTF-8. Use when desired when  XCN_CERT_NAME_STR_FORCE_UTF8_DIR_STR_FLAG is the default behavior.

### -field XCN_CERT_NAME_STR_ENABLE_PUNYCODE_FLAG:0x200000

### -field XCN_CERT_NAME_STR_DS_ESCAPED:0x800000

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-enumerations">CertEnroll Enumerations</a>



<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-ix500distinguishedname">IX500DistinguishedName</a>
