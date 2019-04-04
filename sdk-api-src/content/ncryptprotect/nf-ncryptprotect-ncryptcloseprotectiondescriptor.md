---
UID: NF:ncryptprotect.NCryptCloseProtectionDescriptor
title: NCryptCloseProtectionDescriptor function (ncryptprotect.h)
author: windows-sdk-content
description: Zeros and frees a protection descriptor object and releases its handle.
old-location: security\ncryptcloseprotectiondescriptor.htm
tech.root: SecCNG
ms.assetid: 523FD83E-85A3-4A0E-BA8D-2F27F82C1072
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NCryptCloseProtectionDescriptor, NCryptCloseProtectionDescriptor function [Security], ncryptprotect/NCryptCloseProtectionDescriptor, security.ncryptcloseprotectiondescriptor
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
 - NCryptCloseProtectionDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NCryptCloseProtectionDescriptor function


## -description


The <b>NCryptCloseProtectionDescriptor</b> function zeros and frees a protection descriptor object and releases its handle.


## -parameters




### -param hDescriptor [in]

Handle of a protection descriptor created by calling <a href="https://msdn.microsoft.com/BA6B15AC-2CD8-4D9A-817F-65CF9C09D22C">NCryptCreateProtectionDescriptor</a>.


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
<dt><b>NTE_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified by the <i>hDescriptor</i> parameter cannot be <b>NULL</b> and it must represent a valid descriptor.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/591C7361-334E-4A65-8616-C0ED3BBC2297">CNG DPAPI Functions</a>



<a href="https://msdn.microsoft.com/BA6B15AC-2CD8-4D9A-817F-65CF9C09D22C">NCryptCreateProtectionDescriptor</a>
 

 

