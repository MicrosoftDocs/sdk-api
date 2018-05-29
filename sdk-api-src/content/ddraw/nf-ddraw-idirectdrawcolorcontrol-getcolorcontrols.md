---
UID: NF:ddraw.IDirectDrawColorControl.GetColorControls
title: IDirectDrawColorControl::GetColorControls
author: windows-sdk-content
description: Retrieves the current color-control settings that are associated with an overlay or a primary surface.
old-location: directdraw\idirectdrawcolorcontrol_getcolorcontrols.htm
old-project: directdraw
ms.assetid: 16ac7bef-e88c-47da-8db9-9e6258a381a0
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: GetColorControls, GetColorControls method [DirectDraw], GetColorControls method [DirectDraw],IDirectDrawColorControl interface, IDirectDrawColorControl interface [DirectDraw],GetColorControls method, IDirectDrawColorControl.GetColorControls, IDirectDrawColorControl::GetColorControls, ddraw/IDirectDrawColorControl::GetColorControls, directdraw.idirectdrawcolorcontrol_getcolorcontrols
ms.prod: windows
ms.technology: windows-sdk
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
-	IDirectDrawColorControl.GetColorControls
product: Windows
targetos: Windows
req.lib: Ddraw.lib
req.dll: Ddraw.dll
req.irql: 
---

# IDirectDrawColorControl::GetColorControls


## -description


Retrieves the current color-control settings that are associated with an overlay or a primary surface.


## -parameters






#### - lpColorControl [in, out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff549237">DDCOLORCONTROL</a> structure that receives the current control settings.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_UNSUPPORTED</li>
</ul>



## -remarks



The <b>dwFlags</b> member of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549237">DDCOLORCONTROL</a> structure indicates which of the color-control options are supported.


You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetColorControls</b> method.




## -see-also




<a href="https://msdn.microsoft.com/e9bd0dc6-2d8a-452b-894d-72a3d7a20100">IDirectDrawColorControl</a>
 

 

