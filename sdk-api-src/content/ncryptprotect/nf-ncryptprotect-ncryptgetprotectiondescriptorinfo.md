---
UID: NF:ncryptprotect.NCryptGetProtectionDescriptorInfo
title: NCryptGetProtectionDescriptorInfo function (ncryptprotect.h)
description: Retrieves a protection descriptor rule string.
helpviewer_keywords: ["NCRYPT_PROTECTION_INFO_TYPE_DESCRIPTOR_STRING","NCryptGetProtectionDescriptorInfo","NCryptGetProtectionDescriptorInfo function [Security]","ncryptprotect/NCryptGetProtectionDescriptorInfo","security.ncryptgetprotectiondescriptorinfo"]
old-location: security\ncryptgetprotectiondescriptorinfo.htm
tech.root: security
ms.assetid: EF4777D5-E218-4868-8D25-58E0EF8C9D30
ms.date: 12/05/2018
ms.keywords: NCRYPT_PROTECTION_INFO_TYPE_DESCRIPTOR_STRING, NCryptGetProtectionDescriptorInfo, NCryptGetProtectionDescriptorInfo function [Security], ncryptprotect/NCryptGetProtectionDescriptorInfo, security.ncryptgetprotectiondescriptorinfo
req.header: ncryptprotect.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: NCrypt.lib
req.dll: NCrypt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NCryptGetProtectionDescriptorInfo
 - ncryptprotect/NCryptGetProtectionDescriptorInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptGetProtectionDescriptorInfo
---

# NCryptGetProtectionDescriptorInfo function


## -description

The <b>NCryptGetProtectionDescriptorInfo</b> function retrieves a protection descriptor rule string.

## -parameters

### -param hDescriptor [in]

Protection descriptor handle created by calling <a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>.

### -param pMemPara [in, optional]

Pointer to an <a href="/windows/desktop/api/ncrypt/ns-ncrypt-ncrypt_alloc_para">NCRYPT_ALLOC_PARA</a> structure that you can use to specify custom memory management functions. If you set this argument to <b>NULL</b>, the <a href="/windows/desktop/api/winbase/nf-winbase-localalloc">LocalAlloc</a> function is used internally to allocate memory and your application must call <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> to release memory pointed to by the <i>ppvInfo</i> parameter.

### -param dwInfoType

Specifies how to return descriptor information to the  <i>ppvInfo</i> parameter. This can be the following value:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NCRYPT_PROTECTION_INFO_TYPE_DESCRIPTOR_STRING"></a><a id="ncrypt_protection_info_type_descriptor_string"></a><dl>
<dt><b>NCRYPT_PROTECTION_INFO_TYPE_DESCRIPTOR_STRING</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppvInfo</i> argument returns the descriptor rule string.

</td>
</tr>
</table>

### -param ppvInfo [out]

Pointer to the descriptor information.

## -returns

Returns a status code that indicates the success or failure of the function. Possible return codes include, but are not limited to, the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppvInfo</i> parameter cannot be <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
An unsupported value was specified in the <i>dwInfoType</i> parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hDescriptor</i> parameter is not valid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>