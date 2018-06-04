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

# _DD_MISCELLANEOUS2CALLBACKS structure


## -description


The DD_MISCELLANEOUS2CALLBACKS structure is used to return the addresses of miscellaneous callback routines. These routines are new for Microsoft DirectX 7.0 and later and are exposed through <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> by responding to the GUID_Miscellaneous2Callbacks GUID.


## -struct-fields




### -field dwSize

Specifies the size, in bytes, of this structure.


### -field dwFlags

Indicates which miscellaneous callback functions the driver implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_MISC2CB32_CREATESURFACEEX</dt>
<dt>DDHAL_MISC2CB32_GETDRIVERSTATE</dt>
<dt>DDHAL_MISC2CB32_DESTROYDDLOCAL</dt>
</dl>



### -field AlphaBlt

Unused and must be set to <b>NULL</b>. 


### -field CreateSurfaceEx

Points to the driver's <a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a> implementation. This callback creates an association between a DirectDraw surface and a small integer handle. 


### -field GetDriverState

Points to the driver's <a href="https://msdn.microsoft.com/6e1b0bce-1ac5-46e7-ae25-b0d3ce8580a0">D3dGetDriverState</a> implementation. 


### -field DestroyDDLocal

Points to the driver's <a href="https://msdn.microsoft.com/c68b924b-422d-4a01-8dac-674835833798">D3dDestroyDDLocal</a> implementation. Used to destroy the local copy of the device context. 


## -see-also




<a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a>



<a href="https://msdn.microsoft.com/c68b924b-422d-4a01-8dac-674835833798">D3dDestroyDDLocal</a>



<a href="https://msdn.microsoft.com/6e1b0bce-1ac5-46e7-ae25-b0d3ce8580a0">D3dGetDriverState</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

