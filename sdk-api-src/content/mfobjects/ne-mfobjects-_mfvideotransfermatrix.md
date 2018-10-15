---
UID: NE:mfobjects._MFVideoTransferMatrix
title: "_MFVideoTransferMatrix"
author: windows-sdk-content
description: Describes the conversion matrices between Y'PbPr (component video) and studio R'G'B'.
old-location: mf\mfvideotransfermatrix.htm
tech.root: medfound
ms.assetid: 08a05ee8-b053-4480-b7f9-6d96e541ccd9
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: 08a05ee8-b053-4480-b7f9-6d96e541ccd9, MFVideoTransferMatrix, MFVideoTransferMatrix enumeration [Media Foundation], MFVideoTransferMatrix_BT601, MFVideoTransferMatrix_BT709, MFVideoTransferMatrix_ForceDWORD, MFVideoTransferMatrix_Last, MFVideoTransferMatrix_SMPTE240M, MFVideoTransferMatrix_Unknown, _MFVideoTransferMatrix, mf.mfvideotransfermatrix, mfobjects/MFVideoTransferMatrix, mfobjects/MFVideoTransferMatrix_BT601, mfobjects/MFVideoTransferMatrix_BT709, mfobjects/MFVideoTransferMatrix_ForceDWORD, mfobjects/MFVideoTransferMatrix_Last, mfobjects/MFVideoTransferMatrix_SMPTE240M, mfobjects/MFVideoTransferMatrix_Unknown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - mfobjects.h
api_name:
 - MFVideoTransferMatrix
product: Windows
targetos: Windows
req.typenames: MFVideoTransferMatrix
req.redist: 
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
 

 

