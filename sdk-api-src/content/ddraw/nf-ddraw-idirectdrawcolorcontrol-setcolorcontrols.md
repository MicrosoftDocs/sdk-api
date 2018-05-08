---
UID: NF:ddraw.IDirectDrawColorControl.SetColorControls
title: IDirectDrawColorControl::SetColorControls
author: windows-driver-content
description: Sets the color-control options for an overlay or a primary surface.
old-location: directdraw\idirectdrawcolorcontrol_setcolorcontrols.htm
old-project: directdraw
ms.assetid: de6f8266-d712-40bd-8230-cf5800cf8926
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDirectDrawColorControl interface [DirectDraw],SetColorControls method, IDirectDrawColorControl.SetColorControls, IDirectDrawColorControl::SetColorControls, SetColorControls, SetColorControls method [DirectDraw], SetColorControls method [DirectDraw],IDirectDrawColorControl interface, ddraw/IDirectDrawColorControl::SetColorControls, directdraw.idirectdrawcolorcontrol_setcolorcontrols
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
req.typenames: DEDUP_CONTAINER_EXTENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ddraw.dll
api_name:
-	IDirectDrawColorControl.SetColorControls
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawColorControl::SetColorControls


## -description


Sets the color-control options for an overlay or a primary surface.


## -parameters






#### - lpColorControl [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549237">DDCOLORCONTROL</a> structure that contains the new control settings to apply.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetColorControls</b> method.




## -see-also




<a href="https://msdn.microsoft.com/e9bd0dc6-2d8a-452b-894d-72a3d7a20100">IDirectDrawColorControl</a>
 

 

