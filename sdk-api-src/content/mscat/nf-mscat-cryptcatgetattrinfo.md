---
UID: NF:mscat.CryptCATGetAttrInfo
title: CryptCATGetAttrInfo function (mscat.h)
description: Retrieves information about an attribute of a member of a catalog.
helpviewer_keywords: ["CryptCATGetAttrInfo","CryptCATGetAttrInfo function [Security]","mscat/CryptCATGetAttrInfo","security.cryptcatgetattrinfo"]
old-location: security\cryptcatgetattrinfo.htm
tech.root: security
ms.assetid: e36966ea-741e-4380-85cd-5a3c9db38e6d
ms.date: 12/05/2018
ms.keywords: CryptCATGetAttrInfo, CryptCATGetAttrInfo function [Security], mscat/CryptCATGetAttrInfo, security.cryptcatgetattrinfo
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
 - CryptCATGetAttrInfo
 - mscat/CryptCATGetAttrInfo
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
 - CryptCATGetAttrInfo
---

# CryptCATGetAttrInfo function


## -description

<p class="CCE_Message">[The <b>CryptCATGetAttrInfo</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATGetAttrInfo</b> function retrieves information about an attribute of a member of a catalog.

## -parameters

### -param hCatalog [in]

The handle of the catalog that contains the member to retrieve the attribute information for. This handle is obtained by calling the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> function. This parameter is required and cannot be <b>NULL</b>.

### -param pCatMember [in]

A pointer to a [CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember) structure that represents the member to retrieve the attribute information for. This can be obtained by calling the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatgetmemberinfo">CryptCATGetMemberInfo</a> function. This parameter is required and cannot be <b>NULL</b>.

### -param pwszReferenceTag [in]

A pointer to a null-terminated Unicode string that contains the name of the attribute to retrieve the information for. This parameter is required and cannot be <b>NULL</b>.

## -returns

This function returns a pointer to a [CRYPTCATATTRIBUTE](/windows/desktop/api/mscat/ns-mscat-cryptcatattribute) structure that contains the attribute information. If the function fails, it returns <b>NULL</b>.


<div class="alert"><b>Important</b>  Do not free the returned pointer nor any of the members pointed to by the returned pointer.</div>
<div> </div>



If this function returns <b>NULL</b>, additional error information can be obtained by calling the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function. <b>GetLastError</b> will return one of the following error codes.



<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The member or the attribute could not be found.

</td>
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
</table>

## -see-also

[CRYPTCATATTRIBUTE](/windows/desktop/api/mscat/ns-mscat-cryptcatattribute)



[CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember)



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatgetmemberinfo">CryptCATGetMemberInfo</a>



<a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a>