---
UID: NF:ddraw.IDirectDrawClipper.SetHWnd
title: IDirectDrawClipper::SetHWnd
author: windows-sdk-content
description: Sets the window handle that the clipper object uses to obtain clipping information.
old-location: directdraw\idirectdrawclipper_sethwnd.htm
tech.root: directdraw
ms.assetid: 7683bccd-3f5c-4098-9041-9c66853cda0e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDirectDrawClipper interface [DirectDraw],SetHWnd method, IDirectDrawClipper.SetHWnd, IDirectDrawClipper::SetHWnd, SetHWnd, SetHWnd method [DirectDraw], SetHWnd method [DirectDraw],IDirectDrawClipper interface, ddraw/IDirectDrawClipper::SetHWnd, directdraw.idirectdrawclipper_sethwnd
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
 - IDirectDrawClipper.SetHWnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawClipper::SetHWnd


## -description


Sets the window handle that the clipper object uses to obtain clipping information.


## -parameters




### -param arg1

TBD


### -param arg2

TBD




#### - dwFlags [in]

Currently not used and must be set to 0.


#### - hWnd [in]

Window handle that obtains the clipping information.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDCLIPLIST</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>SetHWnd</b> method.




## -see-also




<a href="https://msdn.microsoft.com/2e93583a-59a8-4a0f-9299-ed57fdcebf33">IDirectDrawClipper</a>
 

 

