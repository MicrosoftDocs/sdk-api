---
UID: NF:ddraw.IDirectDrawSurface7.Initialize
title: IDirectDrawSurface7::Initialize
author: windows-sdk-content
description: Initializes a DirectDrawSurface object.
old-location: directdraw\idirectdrawsurface7_initialize.htm
tech.root: directdraw
ms.assetid: 98b9a05f-ff61-4c58-9c09-625077eb64ad
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],Initialize method, IDirectDrawSurface7.Initialize, IDirectDrawSurface7::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::Initialize, directdraw.idirectdrawsurface7_initialize
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
 - IDirectDrawSurface7.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDrawSurface7::Initialize


## -description


Initializes a DirectDrawSurface object.


## -parameters




### -param arg1 [in]

A pointer to the DirectDraw object to associate with the DirectDrawSurface object.


### -param arg2 [in]

A pointer to a <a href="https://msdn.microsoft.com/507c557f-eb3a-429c-a738-8d715e5d71d3">DDSURFACEDESC2</a> structure that describes how to initialize this surface.


## -returns



This method returns DDERR_ALREADYINITIALIZED.

This method is provided for compliance with the Component Object Model (COM). Because the DirectDrawSurface object is initialized when it is created, this method always returns DDERR_ALREADYINITIALIZED.




## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the  <b>Initialize</b> method.




## -see-also




<a href="https://msdn.microsoft.com/be686d56-c242-4228-ac8e-8f764ad29756">IDirectDrawSurface7</a>
 

 

