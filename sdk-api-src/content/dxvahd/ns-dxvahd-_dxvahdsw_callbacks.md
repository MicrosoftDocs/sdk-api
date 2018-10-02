---
UID: NS:dxvahd._DXVAHDSW_CALLBACKS
title: "_DXVAHDSW_CALLBACKS"
author: windows-sdk-content
description: Contains pointers to functions implemented by a software plug-in for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).
old-location: mf\dxvahdsw_callbacks.htm
tech.root: MedFound
ms.assetid: 74c329cc-af54-4cf8-8cb6-eed9e96db4c5
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: DXVAHDSW_CALLBACKS, DXVAHDSW_CALLBACKS structure [Media Foundation], _DXVAHDSW_CALLBACKS, dxvahd/DXVAHDSW_CALLBACKS, mf.dxvahdsw_callbacks
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxvahd.h
api_name:
 - DXVAHDSW_CALLBACKS
product: Windows
targetos: Windows
req.typenames: DXVAHDSW_CALLBACKS
req.redist: 
---

# _DXVAHDSW_CALLBACKS structure


## -description


Contains pointers to functions implemented by a software plug-in for Microsoft DirectX Video Acceleration High Definition (DXVA-HD).


## -struct-fields




### -field CreateDevice

Function pointer of type <a href="https://msdn.microsoft.com/f76539c8-13a8-4608-87a6-4947f5debb02">PDXVAHDSW_CreateDevice</a>.


### -field ProposeVideoPrivateFormat

Function pointer of type <a href="https://msdn.microsoft.com/b543f05f-40fc-4bdf-ae53-9a451d3bdf2a">PDXVAHDSW_ProposeVideoPrivateFormat</a>.
          


### -field GetVideoProcessorDeviceCaps

Function pointer of type <a href="https://msdn.microsoft.com/09753e3b-7235-4204-ad08-a083a7db4a2b">PDXVAHDSW_GetVideoProcessorDeviceCaps</a>.
          


### -field GetVideoProcessorOutputFormats

Function pointer of type <a href="https://msdn.microsoft.com/d7f767d2-c645-4ade-9b0c-0d5436cf0cfe">PDXVAHDSW_GetVideoProcessorOutputFormats</a>.
          


### -field GetVideoProcessorInputFormats

Function pointer of type <a href="https://msdn.microsoft.com/3d24da29-0fdb-4084-9810-1a0c9b04768b">PDXVAHDSW_GetVideoProcessorInputFormats</a>.
          


### -field GetVideoProcessorCaps

Function pointer of type <a href="https://msdn.microsoft.com/d32fd5e7-b8e8-431f-bc74-b75288ceb01f">PDXVAHDSW_GetVideoProcessorCaps</a>.
          


### -field GetVideoProcessorCustomRates

Function pointer of type <a href="https://msdn.microsoft.com/0b633dcc-c6eb-47e5-b43b-b2a6cb66abf6">PDXVAHDSW_GetVideoProcessorCustomRates</a>.
          


### -field GetVideoProcessorFilterRange

Function pointer of type <a href="https://msdn.microsoft.com/3c28ffcf-dad5-4ed1-8b04-12e22fd566a4">PDXVAHDSW_GetVideoProcessorFilterRange</a>.


### -field DestroyDevice

Function pointer of type <a href="https://msdn.microsoft.com/1d0cc0a4-effb-4dea-b6ba-ca1a4e1e394e">PDXVAHDSW_DestroyDevice</a>.


### -field CreateVideoProcessor

Function pointer of type <a href="https://msdn.microsoft.com/69ddcfc4-e91a-4ad5-ac0f-41683352d55a">PDXVAHDSW_CreateVideoProcessor</a>.


### -field SetVideoProcessBltState

Function pointer of type <a href="https://msdn.microsoft.com/604af2f8-42e8-465c-a49f-8c6c9bcc84dd">PDXVAHDSW_SetVideoProcessBltState</a>.


### -field GetVideoProcessBltStatePrivate

Function pointer of type <a href="https://msdn.microsoft.com/32154457-5270-4e60-a16c-bca72c6a9673">PDXVAHDSW_GetVideoProcessBltStatePrivate</a>.
          


### -field SetVideoProcessStreamState

Function pointer of type <a href="https://msdn.microsoft.com/1fbecdbd-9f04-4d1e-82a6-4c6ce522cdaf">PDXVAHDSW_SetVideoProcessStreamState</a>.


### -field GetVideoProcessStreamStatePrivate

Function pointer of type <a href="https://msdn.microsoft.com/db751314-8c3c-4969-87c4-0b2b2201ce20">PDXVAHDSW_GetVideoProcessStreamStatePrivate</a>.


### -field VideoProcessBltHD

Function pointer of type <a href="https://msdn.microsoft.com/94e6b59f-dd00-4d32-b1ca-a592a67cd0ec">PDXVAHDSW_VideoProcessBltHD</a>.


### -field DestroyVideoProcessor

Function pointer of type <a href="https://msdn.microsoft.com/46667a66-3638-4cf0-9966-3e659d00f914">PDXVAHDSW_DestroyVideoProcessor</a>.


## -remarks



If you provide a software plug-in for DXVA-HD, the plug-in must implement a set of functions that are defined by the function pointer types in this structure.

At initialization, the   DXVA-HD runtime calls the plug-in device's <a href="https://msdn.microsoft.com/1290daa0-a2dd-4067-b74d-e1b3e3edb321">PDXVAHDSW_Plugin</a> function. This function fills in a <b>DXVAHDSW_CALLBACKS</b> structure with pointers to  the set of functions that are implemented by the plug-in device. When the application calls DXVA-HD methods, the DXVA-HD runtime calls the corresponding plug-in functions.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/584c087e-53f0-42d8-99ed-a0d013379363">Direct3D Video Structures</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/1290daa0-a2dd-4067-b74d-e1b3e3edb321">PDXVAHDSW_Plugin</a>
 

 

