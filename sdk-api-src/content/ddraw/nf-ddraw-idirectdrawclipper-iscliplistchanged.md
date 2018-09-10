---
UID: NF:ddraw.IDirectDrawClipper.IsClipListChanged
title: IDirectDrawClipper::IsClipListChanged
author: windows-sdk-content
description: Retrieves the status of the clip list if a window handle is associated with a DirectDrawClipper object.
old-location: directdraw\idirectdrawclipper_iscliplistchanged.htm
tech.root: directdraw
ms.assetid: d394b638-6015-47d8-89ea-2ed71611ddb3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirectDrawClipper interface [DirectDraw],IsClipListChanged method, IDirectDrawClipper.IsClipListChanged, IDirectDrawClipper::IsClipListChanged, IsClipListChanged, IsClipListChanged method [DirectDraw], IsClipListChanged method [DirectDraw],IDirectDrawClipper interface, ddraw/IDirectDrawClipper::IsClipListChanged, directdraw.idirectdrawclipper_iscliplistchanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ddraw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ddraw.dll
api_name:
 - IDirectDrawClipper.IsClipListChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawClipper::IsClipListChanged


## -description


Retrieves the status of the clip list if a window handle is associated with a DirectDrawClipper object.


## -parameters






#### - lpbChanged [out]

A pointer to a variable that receives the status of the clip list. This parameter is TRUE if the clip list has changed, and FALSE otherwise.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>IsClipListChanged</b> method.




## -see-also




<a href="https://msdn.microsoft.com/2e93583a-59a8-4a0f-9299-ed57fdcebf33">IDirectDrawClipper</a>
 

 

