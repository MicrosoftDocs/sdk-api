---
UID: NF:mscat.CryptCATPutMemberInfo
title: CryptCATPutMemberInfo function (mscat.h)
description: Allocates memory for a catalog member and adds it to the catalog.
helpviewer_keywords: ["CryptCATPutMemberInfo","CryptCATPutMemberInfo function [Security]","mscat/CryptCATPutMemberInfo","security.cryptcatputmemberinfo"]
old-location: security\cryptcatputmemberinfo.htm
tech.root: security
ms.assetid: bfc10577-e32e-4b2e-ad24-1d0a85c6730a
ms.date: 12/05/2018
ms.keywords: CryptCATPutMemberInfo, CryptCATPutMemberInfo function [Security], mscat/CryptCATPutMemberInfo, security.cryptcatputmemberinfo
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
 - CryptCATPutMemberInfo
 - mscat/CryptCATPutMemberInfo
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
 - CryptCATPutMemberInfo
---

# CryptCATPutMemberInfo function


## -description

<p class="CCE_Message">[The  <b>CryptCATPutMemberInfo</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATPutMemberInfo</b> function allocates memory for a catalog member and adds it to the catalog.

## -parameters

### -param hCatalog [in]

A handle to the catalog obtained from the <a href="/windows/desktop/api/mscat/nf-mscat-cryptcatopen">CryptCATOpen</a> or <a href="/windows/desktop/api/mscat/nf-mscat-cryptcathandlefromstore">CryptCATHandleFromStore</a> function.

### -param pwszFileName [in, optional]

A pointer to a null-terminated string for the catalog file name.

### -param pwszReferenceTag [in]

A pointer to a null-terminated string that contains the name of the member.

### -param pgSubjectType [in]

A GUID for the subject type of the member.

### -param dwCertVersion [in]

A value that specifies the certificate version.

### -param cbSIPIndirectData [in]

A value that specifies the number of bytes in the <i>pbSIPIndirectData</i> buffer.

### -param pbSIPIndirectData [in]

A pointer to  a memory buffer for <a href="/windows/desktop/SecGloss/s-gly">subject interface package</a> (SIP)-indirect data.

## -returns

A pointer to a [CRYPTCATMEMBER](/windows/desktop/api/mscat/ns-mscat-cryptcatmember) structure that contains the assigned member. The caller must not free this pointer or any of its members.


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