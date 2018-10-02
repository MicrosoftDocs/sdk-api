---
UID: NF:ncryptprotect.NCryptGetProtectionDescriptorInfo
title: NCryptGetProtectionDescriptorInfo function
author: windows-sdk-content
description: Retrieves a protection descriptor rule string.
old-location: security\ncryptgetprotectiondescriptorinfo.htm
tech.root: SecCNG
ms.assetid: EF4777D5-E218-4868-8D25-58E0EF8C9D30
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: NCRYPT_PROTECTION_INFO_TYPE_DESCRIPTOR_STRING, NCryptGetProtectionDescriptorInfo, NCryptGetProtectionDescriptorInfo function [Security], ncryptprotect/NCryptGetProtectionDescriptorInfo, security.ncryptgetprotectiondescriptorinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - NCrypt.dll
api_name:
 - NCryptGetProtectionDescriptorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptGetProtectionDescriptorInfo function


## -description


The <b>NCryptGetProtectionDescriptorInfo</b> function retrieves a protection descriptor rule string.


## -parameters




### -param hDescriptor [in]

Protection descriptor handle created by calling <a href="https://msdn.microsoft.com/BA6B15AC-2CD8-4D9A-817F-65CF9C09D22C">NCryptCreateProtectionDescriptor</a>.


### -param pMemPara [in, optional]

Pointer to an <a href="https://msdn.microsoft.com/4F546F51-E4DE-4703-B1D1-F84165C3C31B">NCRYPT_ALLOC_PARA</a> structure that you can use to specify custom memory management functions. If you set this argument to <b>NULL</b>, the <a href="https://msdn.microsoft.com/da8cd2be-ff4c-4da5-813c-8759a58228c9">LocalAlloc</a> function is used internally to allocate memory and your application must call <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a> to release memory pointed to by the <i>ppvInfo</i> parameter.


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




<a href="https://msdn.microsoft.com/591C7361-334E-4A65-8616-C0ED3BBC2297">CNG DPAPI Functions</a>



<a href="https://msdn.microsoft.com/BA6B15AC-2CD8-4D9A-817F-65CF9C09D22C">NCryptCreateProtectionDescriptor</a>
 

 

