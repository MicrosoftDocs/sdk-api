---
UID: NF:d2d1.ID2D1RenderTarget.GetTags
title: ID2D1RenderTarget::GetTags
author: windows-sdk-content
description: Gets the label for subsequent drawing operations.
old-location: direct2d\ID2D1RenderTarget_GetTags.htm
tech.root: direct2d
ms.assetid: 71da439f-4666-4e49-93f8-26acd222ed1e
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: GetTags, GetTags method [Direct2D], GetTags method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],GetTags method, ID2D1RenderTarget.GetTags, ID2D1RenderTarget::GetTags, d2d1/ID2D1RenderTarget::GetTags, direct2d.ID2D1RenderTarget_GetTags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.GetTags
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- d2d1.h
: 
- ID2D1RenderTarget.GetTags
: 
---

# ID2D1RenderTarget::GetTags


## -description


Gets the label for subsequent drawing operations.


## -parameters




### -param tag1 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4f363295-f140-4149-ba78-3abbc56eebe8">D2D1_TAG</a>*</b>

When this method returns, contains the first label for subsequent drawing operations. This parameter is passed uninitialized. If <b>NULL</b> is specified, no value is retrieved for this parameter. 


### -param tag2 [out, optional]

Type: <b><a href="https://msdn.microsoft.com/4f363295-f140-4149-ba78-3abbc56eebe8">D2D1_TAG</a>*</b>

When this method returns, contains the second label for subsequent drawing operations. This parameter is passed uninitialized. If <b>NULL</b> is specified, no value is retrieved for this parameter.


## -returns



This method does not return a value.




## -remarks



If the same address is passed for both parameters, both parameters receive the value of the second tag. 




## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

