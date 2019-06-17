---
UID: NF:ddraw.IDirectDrawPalette.Initialize
title: IDirectDrawPalette::Initialize (ddraw.h)
author: windows-sdk-content
description: Initializes the DirectDrawPalette object.
old-location: directdraw\idirectdrawpalette_initialize.htm
tech.root: directdraw
ms.assetid: e0ad7ea1-759d-48e9-8d15-6601d9b15588
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDirectDrawPalette interface [DirectDraw],Initialize method, IDirectDrawPalette.Initialize, IDirectDrawPalette::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDrawPalette interface, ddraw/IDirectDrawPalette::Initialize, directdraw.idirectdrawpalette_initialize
ms.topic: method
f1_keywords: ["ddraw/IDirectDrawPalette.Initialize"]
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
 - IDirectDrawPalette.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawPalette::Initialize


## -description


Initializes the DirectDrawPalette object.


## -parameters




### -param arg1 [in]

A pointer to the DirectDraw object to associate with the DirectDrawPalette object.


### -param arg2 [in]

Currently not used and must be set to 0.


### -param arg3 [out]

Currently not used and must be set to NULL.


## -returns



This method returns DDERR_ALREADYINITIALIZED.

This method is provided for compliance with the Component Object Model (COM). Because the DirectDrawPalette object is initialized when it is created, this method always returns DDERR_ALREADYINITIALIZED.




## -remarks



You must use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://docs.microsoft.com/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress">GetProcAddress</a> to access the <b>Initialize</b> method.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddraw/nn-ddraw-idirectdrawpalette">IDirectDrawPalette</a>
 

 

