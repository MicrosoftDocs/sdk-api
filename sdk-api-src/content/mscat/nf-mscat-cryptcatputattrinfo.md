---
UID: NF:mscat.CryptCATPutAttrInfo
title: CryptCATPutAttrInfo function (mscat.h)
description: Allocates memory for an attribute and adds it to a catalog member.
helpviewer_keywords: ["CRYPTCAT_ATTR_AUTHENTICATED","CRYPTCAT_ATTR_DATAASCII","CRYPTCAT_ATTR_DATABASE64","CRYPTCAT_ATTR_DATAREPLACE","CRYPTCAT_ATTR_NAMEASCII","CRYPTCAT_ATTR_NAMEOBJID","CRYPTCAT_ATTR_UNAUTHENTICATED","CryptCATPutAttrInfo","CryptCATPutAttrInfo function [Security]","mscat/CryptCATPutAttrInfo","security.cryptcatputattrinfo"]
old-location: security\cryptcatputattrinfo.htm
tech.root: security
ms.assetid: 13d5cdb4-2a15-4442-9e11-c3f76ca03f7e
ms.date: 12/05/2018
ms.keywords: CRYPTCAT_ATTR_AUTHENTICATED, CRYPTCAT_ATTR_DATAASCII, CRYPTCAT_ATTR_DATABASE64, CRYPTCAT_ATTR_DATAREPLACE, CRYPTCAT_ATTR_NAMEASCII, CRYPTCAT_ATTR_NAMEOBJID, CRYPTCAT_ATTR_UNAUTHENTICATED, CryptCATPutAttrInfo, CryptCATPutAttrInfo function [Security], mscat/CryptCATPutAttrInfo, security.cryptcatputattrinfo
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptCATPutAttrInfo
 - mscat/CryptCATPutAttrInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATPutAttrInfo
---

# CryptCATPutAttrInfo function


## -description

<p class="CCE_Message">[The  <b>CryptCATPutAttrInfo</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATPutAttrInfo</b> function allocates memory for  an attribute and adds it to a catalog member.

## -parameters

### -param hCatalog [in]

A handle to the catalog obtained from the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> or <a href="/windows/desktop/api/mscat/nf-mscat-cryptcathandlefromstore">CryptCATHandleFromStore</a> function.

### -param pCatMember [in]

A pointer to a [CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember) structure that contains the catalog member.

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
The attribute is a cryptographic <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

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

Upon success, this function returns a pointer to a [CRYPTCATATTRIBUTE](/windows/desktop/api/mscat/ns-mscat-cryptcatattribute) structure that contains the assigned attribute. The caller must not free this pointer or any of its members.


If this function returns <b>NULL</b>, additional error information can be obtained by calling the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. <b>GetLastError</b> will return one of the following error codes.



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