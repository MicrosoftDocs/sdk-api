---
UID: NF:ncryptprotect.NCryptCloseProtectionDescriptor
title: NCryptCloseProtectionDescriptor function (ncryptprotect.h)

description: Zeros and frees a protection descriptor object and releases its handle.
old-location: security\ncryptcloseprotectiondescriptor.htm
tech.root: SecCNG
ms.assetid: 523FD83E-85A3-4A0E-BA8D-2F27F82C1072

ms.date: 12/05/2018
ms.keywords: NCryptCloseProtectionDescriptor, NCryptCloseProtectionDescriptor function [Security], ncryptprotect/NCryptCloseProtectionDescriptor, security.ncryptcloseprotectiondescriptor
ms.topic: function
f1_keywords: 
 - "ncryptprotect/NCryptCloseProtectionDescriptor"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NCryptCloseProtectionDescriptor function


## -description


The <b>NCryptCloseProtectionDescriptor</b> function zeros and frees a protection descriptor object and releases its handle.


## -parameters




### -param hDescriptor [in]

Handle of a protection descriptor created by calling <a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>.


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




<a href="https://docs.microsoft.com/windows/desktop/SecCNG/cng-dpapi-functions">CNG DPAPI Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ncryptprotect/nf-ncryptprotect-ncryptcreateprotectiondescriptor">NCryptCreateProtectionDescriptor</a>
 

 

