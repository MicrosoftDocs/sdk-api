---
UID: NF:mscat.CryptCATPutMemberInfo
title: CryptCATPutMemberInfo function (mscat.h)
author: windows-sdk-content
description: Allocates memory for a catalog member and adds it to the catalog.
old-location: security\cryptcatputmemberinfo.htm
tech.root: SecCrypto
ms.assetid: bfc10577-e32e-4b2e-ad24-1d0a85c6730a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CryptCATPutMemberInfo, CryptCATPutMemberInfo function [Security], mscat/CryptCATPutMemberInfo, security.cryptcatputmemberinfo
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
req.lib: Wintrust.lib
req.dll: Wintrust.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Wintrust.dll
api_name:
 - CryptCATPutMemberInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CryptCATPutMemberInfo function


## -description


<p class="CCE_Message">[The  <b>CryptCATPutMemberInfo</b> function is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CryptCATPutMemberInfo</b> function allocates memory for a catalog member and adds it to the catalog.


## -parameters




### -param hCatalog [in]

A handle to the catalog obtained from the <a href="https://msdn.microsoft.com/e81f3a3d-d5b7-4266-838d-b83e331c8594">CryptCATOpen</a> or <a href="https://msdn.microsoft.com/e9aedc2d-9492-4ed7-9f2d-891997f85f6f">CryptCATHandleFromStore</a> function.


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

A pointer to  a memory buffer for <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">subject interface package</a> (SIP)-indirect data.


## -returns



A pointer to a <a href="https://msdn.microsoft.com/08f663d9-9dc2-4ac9-95c5-7f2ed972eb9b">CRYPTCATMEMBER</a> structure that contains the assigned member. The caller must not free this pointer or any of its members.


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
 



