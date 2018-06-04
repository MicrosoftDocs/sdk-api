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

# _MFVideoTransferMatrix enumeration


## -description



Describes the conversion matrices between Y'PbPr (component video) and studio R'G'B'.




## -enum-fields




### -field MFVideoTransferMatrix_Unknown

Unknown transfer matrix. Treat as MFVideoTransferMatrix_BT709.


### -field MFVideoTransferMatrix_BT709

ITU-R BT.709 transfer matrix.


### -field MFVideoTransferMatrix_BT601

ITU-R BT.601 transfer matrix. Also used for SMPTE 170 and ITU-R BT.470-2 System B,G.


### -field MFVideoTransferMatrix_SMPTE240M

SMPTE 240M transfer matrix.


### -field MFVideoTransferMatrix_BT2020_10


### -field MFVideoTransferMatrix_BT2020_12


### -field MFVideoTransferMatrix_Last

Reserved.


### -field MFVideoTransferMatrix_ForceDWORD

Reserved. This member forces the enumeration type to compile as a <b>DWORD</b> value.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/b268d16d-b4cc-4026-9ba7-805cc5409b95">MF_MT_YUV_MATRIX</a> attribute.

For more information about these values, see the remarks for the <a href="https://msdn.microsoft.com/682fa0c7-8f17-457f-9f8a-dc9190866152">DXVA2_VideoTransferMatrix</a> enumeration, which is the DirectX Video Acceleration (DXVA) equivalent of this enumeration.




## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>



<a href="https://msdn.microsoft.com/b8cfe0d1-013d-4706-bb76-6d426836ab6a">Video Media Types</a>
 

 

