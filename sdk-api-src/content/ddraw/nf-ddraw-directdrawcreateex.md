---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# DirectDrawCreateEx function


## -description


Creates an instance of a DirectDraw object that supports the set of Direct3D interfaces in DirectX 7.0. To use the features of Direct3D in DirectX 7.0, create a DirectDraw object with this function.


## -parameters




### -param lpGuid

TBD


### -param lplpDD [out]

A pointer to a variable to be set to a valid <a href="https://msdn.microsoft.com/1a1164fe-00c2-4469-8346-f86f7f48781e">IDirectDraw7</a> interface pointer if the call succeeds.


### -param iid [in]

This parameter must be set to IID_IDirectDraw7. This function fails and returns DDERR_INVALIDPARAMS if any other interface is specified.


### -param pUnkOuter [in]

Allows for future compatibility with COM aggregation features. Currently, this function returns an error if this parameter is not NULL.


#### - lpGUID [in]

A pointer to the globally unique identifier (GUID) that represents the driver to be created. This can be NULL to indicate the active display driver, or you can pass one of the following flags to restrict the active display driver's behavior for debugging purposes:



#### DDCREATE_EMULATIONONLY

The DirectDraw object uses emulation for all features; it does not take advantage of any hardware-supported features.



#### DDCREATE_HARDWAREONLY

The DirectDraw object never emulates features not supported by the hardware. Attempts to call methods that require unsupported features fail, returning DDERR_UNSUPPORTED.


## -returns



If the function succeeds, the return value is DD_OK.



If it fails, the function can return one of the following error values:

<ul>
<li>DDERR_DIRECTDRAWALREADYCREATED</li>
<li>DDERR_GENERIC</li>
<li>DDERR_INVALIDDIRECTDRAWGUID</li>
<li>DDERR_INVALIDPARAMS</li>
<li>DDERR_NODIRECTDRAWHW</li>
<li>DDERR_OUTOFMEMORY</li>
</ul>



## -remarks



This function attempts to initialize a DirectDraw object, and then sets a pointer to the object if the call succeeds.

On computers with multiple monitors, if you specify NULL for <i>lpGUID</i>, the DirectDraw object runs in emulation mode when the normal cooperative level is set. To make use of hardware acceleration on these computers, specify the device's GUID.

You must use <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> to explicitly link to Ddraw.dll and then use <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> to access the <b>DirectDrawCreateEx</b> function.



