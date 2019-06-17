---
UID: NF:ddraw.IDirectDrawSurface7.Initialize
title: IDirectDrawSurface7::Initialize (ddraw.h)
author: windows-sdk-content
description: Initializes a DirectDrawSurface object.
old-location: directdraw\idirectdrawsurface7_initialize.htm
tech.root: directdraw
ms.assetid: 98b9a05f-ff61-4c58-9c09-625077eb64ad
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawSurface7 interface [DirectDraw],Initialize method, IDirectDrawSurface7.Initialize, IDirectDrawSurface7::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDrawSurface7 interface, ddraw/IDirectDrawSurface7::Initialize, directdraw.idirectdrawsurface7_initialize
ms.topic: method
f1_keywords: ["ddraw/IDirectDrawSurface7.Initialize"]
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
ms.custom: 19H1
---

# IDirectDrawSurface7::Initialize


## -description


Initializes a DirectDrawSurface object.


## -parameters




### -param arg1 [in]

A pointer to the DirectDraw object to associate with the DirectDrawSurface object.


### -param arg2 [in]

A pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/hardware/drivers/ff550340(v=vs.85)">DDSURFACEDESC2</a> structure that describes how to initialize this surface.


## -returns



This method returns DDERR_ALREADYINITIALIZED.

This method is provided for compliance with the Component Object Model (COM). Because the DirectDrawSurface object is initialized when it is created, this method always returns DDERR_ALREADYINITIALIZED.




## -remarks



You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the  <b>Initialize</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdrawsurface7">IDirectDrawSurface7</a>
 

 

