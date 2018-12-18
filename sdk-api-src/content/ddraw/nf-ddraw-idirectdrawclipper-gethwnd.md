---
UID: NF:ddraw.IDirectDrawClipper.GetHWnd
title: IDirectDrawClipper::GetHWnd
author: windows-sdk-content
description: Retrieves the window handle that was previously associated with this DirectDrawClipper object by the IDirectDrawClipper::SetHWnd method.
old-location: directdraw\idirectdrawclipper_gethwnd.htm
tech.root: directdraw
ms.assetid: 025e898f-e160-4485-87cf-f5fbc014e9f1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetHWnd, GetHWnd method [DirectDraw], GetHWnd method [DirectDraw],IDirectDrawClipper interface, IDirectDrawClipper interface [DirectDraw],GetHWnd method, IDirectDrawClipper.GetHWnd, IDirectDrawClipper::GetHWnd, ddraw/IDirectDrawClipper::GetHWnd, directdraw.idirectdrawclipper_gethwnd
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
 - IDirectDrawClipper.GetHWnd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawClipper::GetHWnd


## -description


Retrieves the window handle that was previously associated with this DirectDrawClipper object by the <a href="https://msdn.microsoft.com/7683bccd-3f5c-4098-9041-9c66853cda0e">IDirectDrawClipper::SetHWnd</a> method.



## -parameters






#### - lphWnd [out]

A pointer to a variable that receives the window handle that was previously associated with this DirectDrawClipper object by the <a href="https://msdn.microsoft.com/7683bccd-3f5c-4098-9041-9c66853cda0e">IDirectDrawClipper::SetHWnd</a> method.


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
</ul>



## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>GetHWnd</b> method.




## -see-also




<a href="https://msdn.microsoft.com/2e93583a-59a8-4a0f-9299-ed57fdcebf33">IDirectDrawClipper</a>
 

 

