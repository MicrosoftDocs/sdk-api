---
UID: NF:winber.ber_printf
title: ber_printf function (winber.h)
description: Used to encode a BER element and is similar to sprintf_s.
helpviewer_keywords: ["_ldap_ber_printf","ber_printf","ber_printf function [LDAP]","ldap.ber__printf","ldap.ber_printf","winber/ber_printf"]
old-location: ldap\ber_printf.htm
tech.root: ldap
ms.assetid: 6bae449b-eb75-4598-aacc-65567de67997
ms.date: 12/05/2018
ms.keywords: _ldap_ber_printf, ber_printf, ber_printf function [LDAP], ldap.ber__printf, ldap.ber_printf, winber/ber_printf
req.header: winber.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wldap32.lib
req.dll: Wldap32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ber_printf
 - winber/ber_printf
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ber_printf
---

# ber_printf function


## -description

The <b>ber_printf</b> function is  used to encode a BER element and is similar to  sprintf_s. One important difference is that state data is stored in the <b>BerElement</b> argument so that multiple calls can be made to <b>ber_printf</b> to append to the end of the BER element. The <b>BerElement</b> argument passed to this function must be a pointer to a <b>BerElement</b> returned by 
<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_alloc_t">ber_alloc_t</a>.

## -parameters

### -param pBerElement [in, out]

A pointer to the encoded <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a> structure.

### -param fmt [in]

An encoding format string. For more information, see Remarks.

### -param ...

The values to be encoded as specified by the <i>fmt</i> argument.

## -returns

If the function succeeds, a non-negative number is returned. If the function fails,  -1 is returned.

## -remarks

The format string can contain format characters listed in the following table.

<table>
<tr>
<th> Character</th>
<th>Description</th>
</tr>
<tr>
<td><b>t</b></td>
<td><b>Tag</b>. The next argument is a <b>ber_tag_t</b> that specifies the tag to override the next element written to the <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a>. This works across calls.</td>
</tr>
<tr>
<td><b>b</b></td>
<td><b>Boolean</b>. The next argument is an <b>ber_int_t</b>, that contains either 0 for <b>FALSE</b> or 1 for <b>TRUE</b>. A Boolean element is output. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x01U is used for the element.</td>
</tr>
<tr>
<td><b>e</b></td>
<td><b>Enumerated</b>. The next argument is a <b>ber_int_t</b>, that contains the enumerated value. An enumerated element is output. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x0AU is used for the element.</td>
</tr>
<tr>
<td><b>i</b></td>
<td><b>Integer</b>. The next argument is a <b>ber_int_t</b>, that contains the integer value. An integer element is output. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x02U is used for the element.</td>
</tr>
<tr>
<td><b>n</b></td>
<td><b>Null</b>. No argument is required. An ASN.1 NULL element is output. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x05U is used for the element.</td>
</tr>
<tr>
<td><b>o</b></td>
<td><b>Octet string</b>. The next two arguments are a <b>char*</b>, followed by a <b>ber_len_t</b> with the length of the string. The string may contain <b>NULL</b> bytes and do not have to be zero-terminated. An octet string element is output and no character format conversions on the string data is performed. Passing a <b>NULL</b> pointer followed by a length of 0 is acceptable if a <b>NULL</b> octet string element is required. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x04U is used for the element.</td>
</tr>
<tr>
<td><b>s</b></td>
<td><b>Octet string</b>. The next argument is a <b>char*</b> pointing to a zero-terminated ANSI character string.     The ANSI string characters are converted to UTF-8 format and an octet string element is output, which does not include the trailing '\0' (null) byte.  Passing a <b>NULL</b> pointer is acceptable if a <b>NULL</b> octet string element is required. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x04U is used for the element.</td>
</tr>
<tr>
<td><b>v</b></td>
<td><b>Several octet strings</b>. The next argument is a <b>char**</b>, an array of <b>char*</b> pointers to zero-terminated ANSI strings. The last element in the array must be a <b>NULL</b> pointer. The octet strings do not include the trailing '\0' (null) byte. Be aware that a construct like <b>{</b><b>v</b><b>}</b> is used to get an actual SEQUENCE OF octet strings. The <b>t</b> format modifier cannot be used with this format character.</td>
</tr>
<tr>
<td><b>V</b></td>
<td><b>Several octet strings</b>. A NULL-terminated array of <a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval*</a> is supplied. Be aware that a construct like <b>{</b><b>v</b><b>}</b> is used to get an actual SEQUENCE OF octet strings. The <b>t</b> format modifier cannot be used with this format character.</td>
</tr>
<tr>
<td><b>X</b></td>
<td><b>Bitstring</b>. The next two arguments are a <b>char*</b> pointer to the start of the bitstring, followed by a <b>ber_len_t</b> that contains the number of bits in the bitstring. A bitstring element is output. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x03U is used for the element.</td>
</tr>
<tr>
<td><b>{</b></td>
<td><b>Begin sequence</b>. No argument is required. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x30U is used.</td>
</tr>
<tr>
<td><b>}</b></td>
<td><b>End sequence</b>. No argument is required. The <b>t</b> format modifier cannot be used with this format character.</td>
</tr>
<tr>
<td><b>[</b></td>
<td><b>Begin set</b>. No argument is required. If this format character is not preceded by the <b>t</b> format modifier, the tag 0x31U is used.</td>
</tr>
<tr>
<td><b>]</b></td>
<td><b>End set</b>. No argument is required. The <b>t</b> format modifier cannot be used with this format character.</td>
</tr>
</table>
 

Each left brace (<b>{</b>) character must be paired with a right brace (<b>}</b>) character later in the format string, or in the format string of a subsequent call to <b>ber_printf</b> for that specific <a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a>. The same applies to the left bracket ([) character and right bracket (]) characters.

## -see-also

<a href="/previous-versions/windows/desktop/api/winldap/ns-winldap-berelement">BerElement</a>



<a href="/previous-versions/windows/desktop/ldap/functions">Functions</a>



<a href="/previous-versions/windows/desktop/api/winber/nf-winber-ber_scanf">ber_scanf</a>



<a href="/windows/win32/api/winldap/ns-winldap-ldap_berval">berval</a>

