---
UID: NS:ncrypt.NCRYPT_ALLOC_PARA
title: NCRYPT_ALLOC_PARA
author: windows-sdk-content
description: Enables you to specify custom functions that can be used to allocate and free data.
old-location: security\ncrypt_alloc_para.htm
old-project: seccng
ms.assetid: 4F546F51-E4DE-4703-B1D1-F84165C3C31B
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NCRYPT_ALLOC_PARA, NCRYPT_ALLOC_PARA structure [Security], PNCRYPT_ALLOC_PARA, PNCRYPT_ALLOC_PARA structure pointer [Security], ncrypt/NCRYPT_ALLOC_PARA, ncrypt/PNCRYPT_ALLOC_PARA, security.ncrypt_alloc_para
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ncrypt.h
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
tech.root: 
req.typenames: NCRYPT_ALLOC_PARA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ncrypt.h
api_name:
 - NCRYPT_ALLOC_PARA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NCRYPT_ALLOC_PARA structure


## -description


The <b>NCRYPT_ALLOC_PARA</b> structure enables you to specify custom functions that can be used to allocate and free data. This structure is used in the following functions:
<ul>
<li>
<a href="https://msdn.microsoft.com/EF4777D5-E218-4868-8D25-58E0EF8C9D30">NCryptGetProtectionDescriptorInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8726F92B-34D5-4696-8803-3D7F50F1006D">NCryptProtectSecret</a>
</li>
<li>
<a href="https://msdn.microsoft.com/F532F0ED-36F4-47E3-B478-089CC083E5D1">NCryptUnprotectSecret</a>
</li>
</ul>

## -struct-fields




### -field cbSize

The size, in bytes, of this structure.


### -field pfnAlloc

Address of a custom function that can allocate memory.


### -field pfnFree

Address of a function that can free memory allocated by the function specified by the <b>pfnAlloc</b> member.


## -see-also




<a href="https://msdn.microsoft.com/EF4777D5-E218-4868-8D25-58E0EF8C9D30">NCryptGetProtectionDescriptorInfo</a>



<a href="https://msdn.microsoft.com/8726F92B-34D5-4696-8803-3D7F50F1006D">NCryptProtectSecret</a>



<a href="https://msdn.microsoft.com/F532F0ED-36F4-47E3-B478-089CC083E5D1">NCryptUnprotectSecret</a>
 

 

