---
UID: NF:ddraw.IDirectDraw7.Initialize
title: IDirectDraw7::Initialize
author: windows-sdk-content
description: Initializes a DirectDraw object that was created by using the CoCreateInstance COM function.
old-location: directdraw\idirectdraw7_initialize.htm
tech.root: directdraw
ms.assetid: e641d8e7-ce29-454a-80fc-d404a27e9b63
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IDirectDraw7 interface [DirectDraw],Initialize method, IDirectDraw7.Initialize, IDirectDraw7::Initialize, Initialize, Initialize method [DirectDraw], Initialize method [DirectDraw],IDirectDraw7 interface, ddraw/IDirectDraw7::Initialize, directdraw.idirectdraw7_initialize
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
 - IDirectDraw7.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDirectDraw7::Initialize


## -description


Initializes a DirectDraw object that was created by using the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> COM function.


## -parameters






#### - lpGUID [in]

A pointer to the globally unique identifier (GUID) that this method uses as the DirectDraw interface identifier. 


## -returns



If the method succeeds, the return value is DD_OK.



If it fails, the method can return one of the following error values:

<ul>
<li>DDERR_ALREADYINITIALIZED</li>
<li>DDERR_DIRECTDRAWALREADYCREATED</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDOBJECT</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NODIRECTDRAWHW</li>
<li>DDERR_NODIRECTDRAWSUPPORT</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>
This method is provided for compliance with the Component Object Model (COM). If you already used the <a href="https://msdn.microsoft.com/bad18493-417f-499d-a9a8-719d094be62a">DirectDrawCreate</a> function to create a DirectDraw object, this method returns DDERR_ALREADYINITIALIZED. If you do not call <b>IDirectDraw7::Initialize</b> when you use <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> to create a DirectDraw object, any method that you call afterward returns DDERR_NOTINITIALIZED.




## -remarks



You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>IDirectDraw7::Initialize</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a>
 

 

