---
UID: NF:mscat.CryptCATPutAttrInfo
title: CryptCATPutAttrInfo function
author: windows-sdk-content
description: Allocates memory for an attribute and adds it to a catalog member.
old-location: security\cryptcatputattrinfo.htm
old-project: SecCrypto
ms.assetid: 13d5cdb4-2a15-4442-9e11-c3f76ca03f7e
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: CRYPTCAT_ATTR_AUTHENTICATED, CRYPTCAT_ATTR_DATAASCII, CRYPTCAT_ATTR_DATABASE64, CRYPTCAT_ATTR_DATAREPLACE, CRYPTCAT_ATTR_NAMEASCII, CRYPTCAT_ATTR_NAMEOBJID, CRYPTCAT_ATTR_UNAUTHENTICATED, CryptCATPutAttrInfo, CryptCATPutAttrInfo function [Security], mscat/CryptCATPutAttrInfo, security.cryptcatputattrinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: mscat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: KSP_PINMODE, *PKSP_PINMODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATPutAttrInfo
product: Windows
targetos: Windows
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
req.product: GDI+ 1.1
---

# CryptCATPutAttrInfo function


## -description


<p class="CCE_Message">[The  <b>CryptCATPutAttrInfo</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATPutAttrInfo</b> function allocates memory for  an attribute and adds it to a catalog member.


## -parameters




### -param hCatalog [in]

A handle to the catalog obtained from the <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> or <a href="https://msdn.microsoft.com/e9aedc2d-9492-4ed7-9f2d-891997f85f6f">CryptCATHandleFromStore</a> function.


### -param pCatMember [in]

A pointer to a <a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a> structure that contains the catalog member.


### -param pwszReferenceTag [in]

A pointer to a null-terminated string that contains the name of the attribute.


### -param dwAttrTypeAndAction [in]

A value that represents a bitwise combination of the following flags. The caller must at least specify <b>CRYPTCAT_ATTR_DATABASE64</b> or <b>CRYPTCAT_ATTR_DATAASCII</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_AUTHENTICATED"></a><a id="cryptcat_attr_authenticated"></a><dl>
<dt><b>CRYPTCAT_ATTR_AUTHENTICATED</b></dt>
<dt>0x10000000</dt>
</dl>
</td>
<td width="60%">
The attribute is authenticated.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_UNAUTHENTICATED"></a><a id="cryptcat_attr_unauthenticated"></a><dl>
<dt><b>CRYPTCAT_ATTR_UNAUTHENTICATED</b></dt>
<dt>0x20000000</dt>
</dl>
</td>
<td width="60%">
The attribute is unauthenticated.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_NAMEASCII"></a><a id="cryptcat_attr_nameascii"></a><dl>
<dt><b>CRYPTCAT_ATTR_NAMEASCII</b></dt>
<dt>             0x00000001</dt>
</dl>
</td>
<td width="60%">
The attribute is an ASCII string.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_NAMEOBJID"></a><a id="cryptcat_attr_nameobjid"></a><dl>
<dt><b>CRYPTCAT_ATTR_NAMEOBJID</b></dt>
<dt>             0x00000002</dt>
</dl>
</td>
<td width="60%">
The attribute is a cryptographic <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_DATAASCII"></a><a id="cryptcat_attr_dataascii"></a><dl>
<dt><b>CRYPTCAT_ATTR_DATAASCII</b></dt>
<dt>             0x00010000</dt>
</dl>
</td>
<td width="60%">
The attribute contains simple ASCII characters that should not be decoded.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_DATABASE64"></a><a id="cryptcat_attr_database64"></a><dl>
<dt><b>CRYPTCAT_ATTR_DATABASE64</b></dt>
<dt>            0x00020000</dt>
</dl>
</td>
<td width="60%">
The attribute is in base 64 format.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPTCAT_ATTR_DATAREPLACE"></a><a id="cryptcat_attr_datareplace"></a><dl>
<dt><b>CRYPTCAT_ATTR_DATAREPLACE</b></dt>
<dt>           0x00040000</dt>
</dl>
</td>
<td width="60%">
The attribute replaces the value for an existing attribute.

</td>
</tr>
</table>
 


### -param cbData [in]

A value that specifies the number of bytes in the <i>pbData</i> buffer.


### -param pbData [in]

A pointer to a memory buffer that contains the attribute value.


## -returns



Upon success, this function returns a pointer to a <a href="https://msdn.microsoft.com/41b91303-f3eb-4288-9ad2-98f170680988">CRYPTCATATTRIBUTE</a> structure that contains the assigned attribute. The caller must not free this pointer or any of its members.


If this function returns <b>NULL</b>, additional error information can be obtained by calling the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. <b>GetLastError</b> will return one of the following error codes.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The operating system ran out of memory during the operation.

</td>
</tr>
</table>
 



