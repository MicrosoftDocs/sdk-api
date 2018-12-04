---
UID: NF:winber.ber_scanf
title: ber_scanf function
author: windows-sdk-content
description: The ber_scanf function decodes a BER element in a similar manner as sscanf_s.
old-location: ldap\ber_scanf.htm
tech.root: ldap
ms.assetid: bca69428-27e1-4028-bfcd-ad67bee672cc
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: "_ldap_ber_scanf, ber_scanf, ber_scanf function [LDAP], ldap.ber__scanf, ldap.ber_scanf, winber/ber_scanf"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wldap32.dll
api_name:
 - ber_scanf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ber_scanf function


## -description


The <b>ber_scanf</b> function decodes a BER element in a similar manner as <a href="http://go.microsoft.com/fwlink/p/?linkid=83973">sscanf_s</a>. One important difference is that some state status data is kept with the <b>BerElement</b> argument so that multiple calls can be made to <b>ber_scanf</b> to sequentially read from the BER element. The <b>BerElement</b> argument should be a pointer to a <b>BerElement</b> returned by <a href="https://msdn.microsoft.com/ad6557e9-1683-4ffd-a59e-8f37eb67d089">ber_init</a>.


## -parameters




### -param pBerElement [in, out]

Pointer to the decoded <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


### -param fmt [in]

Encoding format string. For more information, see Remarks section.


### -param arg3 [in]

Pointers to variables used to hold the values decoded as specified by the <i>fmt</i> argument.


## -returns



On error, the function returns LBER_ERROR.




## -remarks



The function interprets the bytes according to the format string <i>fmt</i>, and stores the results in its additional arguments. The format string contains conversion specifications used to direct the interpretation of the BER element. The format string can contain characters listed in the following table.

<table>
<tr>
<th>Character</th>
<th>Description</th>
</tr>
<tr>
<td><b>a</b></td>
<td><b>Octet string</b>. A <b>char**</b> argument must be supplied. Memory is allocated, filled with the contents of the octet string, zero-terminated, and the pointer to the string is stored in the argument. The returned value should be freed using 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a>. The tag of the element must indicate the primitive form (constructed strings are not supported), but is otherwise ignored and discarded during the decoding. This format cannot be used with octet strings which could contain null bytes.</td>
</tr>
<tr>
<td><b>O</b></td>
<td><b>Octet string</b>. A <b>berval**</b> argument must be supplied, which upon return points to an allocated <b>berval</b> that contains the octet string and its length. 
<a href="https://msdn.microsoft.com/9e5a4bb9-568d-48ee-be75-952916c021b1">ber_bvfree</a> should be called to free the allocated memory. The tag of the element must indicate the primitive form (constructed strings are not supported), but is otherwise ignored during the decoding.</td>
</tr>
<tr>
<td><b>b</b></td>
<td><b>Boolean</b>. A pointer to a <b>ber_int_t</b> must be supplied. The <b>ber_int_t</b> value stored will be 0 for FALSE or nonzero for TRUE. The tag of the element must indicate the primitive form, but is otherwise ignored during the decoding.</td>
</tr>
<tr>
<td><b>e</b></td>
<td><b>Enumerated</b>. A pointer to a <b>ber_int_t</b> must be supplied. The tag of the element must indicate the primitive form but is otherwise ignored during the decoding. <b>ber_scanf</b> will return an error if the value of the enumerated value cannot be stored in a <b>ber_int_t</b>.</td>
</tr>
<tr>
<td><b>i</b></td>
<td><b>Integer</b>. A pointer to a <b>ber_int_t</b> must be supplied. The tag of the element must indicate the primitive form, but is otherwise ignored during decoding. <b>ber_scanf</b> will return an error if the integer cannot be stored in a <b>ber_int_t</b>.</td>
</tr>
<tr>
<td><b>B</b></td>
<td><b>Bitstring</b>. A <b>char**</b> argument must be supplied which will point to the allocated bits, followed by a <b>ber_len_t</b> * argument, which will point to the length (in bits) of the bitstring returned. 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a> should be called to free the bitstring. The tag of the element must indicate the primitive form (constructed bitstrings are not supported), but is otherwise ignored during the decoding.</td>
</tr>
<tr>
<td><b>n</b></td>
<td><b>Null</b>. No argument is required. The element is verified to have a zero-length value and is skipped. The tag is ignored.</td>
</tr>
<tr>
<td><b>t</b></td>
<td><b>Tag</b>. A pointer to a <b>ber_tag_t</b> must be supplied. The <b>ber_tag_t</b> value stored will be the tag of the next element in the <i>pBerElement</i>, represented so it can be written using the <b>t</b> format of <a href="https://msdn.microsoft.com/6bae449b-eb75-4598-aacc-65567de67997">ber_printf</a>. The decoding position within the <i>pBerElement</i> argument is unchanged by this.</td>
</tr>
<tr>
<td><b>v</b></td>
<td><b>Several octet strings</b>. A <b>char***</b> argument must be supplied, which upon return points to an allocated null-terminated array of char *'s that contain the octet strings. <b>NULL</b> is stored if the sequence is empty. 
<a href="https://msdn.microsoft.com/3256a202-4245-4bea-a66c-0f28bfe2ef7e">ldap_memfree</a> should be called to free each element of the array and the array itself. The tag of the sequence and of the octet strings are ignored.</td>
</tr>
<tr>
<td><b>V</b></td>
<td><b>Several octet strings</b> (which could contain null bytes). A <b>berval***</b> must be supplied, which upon return points to an allocated NULL-terminated array of <b>berval*</b>'s containing the octet strings and their lengths. <b>NULL</b> is stored if the sequence is empty. 
<a href="https://msdn.microsoft.com/5c2b53e4-257e-4c3f-b712-345e6b33341b">ber_bvecfree</a> can be called to free the allocated memory. The tag of the sequence and of the octet strings are ignored.</td>
</tr>
<tr>
<td><b>x</b></td>
<td><b>Skip element</b>. The next element is skipped. No argument is required.</td>
</tr>
<tr>
<td><b>{</b></td>
<td><b>Begin sequence</b>. No argument is required. The initial sequence tag and length are skipped.</td>
</tr>
<tr>
<td><b>}</b></td>
<td><b>End sequence</b>. No argument is required.</td>
</tr>
<tr>
<td><b>[</b></td>
<td><b>Begin set</b>. No argument is required. The initial set tag and length are skipped.</td>
</tr>
<tr>
<td><b>]</b></td>
<td><b>End set</b>. No argument is required.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a>



<a href="https://msdn.microsoft.com/7a0040ea-f8f3-4378-8371-49768714d762">Functions</a>



<a href="https://msdn.microsoft.com/6bae449b-eb75-4598-aacc-65567de67997">ber_printf</a>



<a href="https://msdn.microsoft.com/1f279905-ab02-4a8b-9b77-e8ea2b56e882">berval</a>
 

 

