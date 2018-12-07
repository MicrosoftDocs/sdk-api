---
UID: NS:dxva2api._DXVA2_ExtendedFormat
title: "_DXVA2_ExtendedFormat"
author: windows-sdk-content
description: Describes the format of a video stream.
old-location: mf\dxva2_extendedformat.htm
tech.root: medfound
ms.assetid: eba2c56b-8951-4dc5-91ae-1371793ce787
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DXVA2_ExtendedFormat, DXVA2_ExtendedFormat structure [Media Foundation], _DXVA2_ExtendedFormat, dxva2api/DXVA2_ExtendedFormat, eba2c56b-8951-4dc5-91ae-1371793ce787, mf.dxva2_extendedformat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: dxva2api.h
req.include-header: 
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
 - dxva2api.h
api_name:
 - DXVA2_ExtendedFormat
product: Windows
targetos: Windows
req.typenames: DXVA2_ExtendedFormat
req.redist: 
---

# _DXVA2_ExtendedFormat structure


## -description


Describes the format of a video stream.
        


## -struct-fields




### -field SampleFormat

Describes the interlacing of the video frames. Contains a value from the <a href="https://msdn.microsoft.com/7d2d38c0-249d-47c3-acda-ba1bec721a5c">DXVA2_SampleFormat</a> enumeration.


### -field VideoChromaSubsampling

Describes the chroma siting. Contains a value from the <a href="https://msdn.microsoft.com/0f9d63fd-46fa-498c-8703-1beeaf09ce86">DXVA2_VideoChromaSubSampling</a> enumeration.


### -field NominalRange

Describes the nominal range of the Y'CbCr or RGB color data. Contains a value from the <a href="https://msdn.microsoft.com/ebc146e4-517f-4413-93dc-66cf4b3a04c3">DXVA2_NominalRange</a> enumeration.


### -field VideoTransferMatrix

Describes the transform from Y'PbPr (component video) to studio R'G'B'. Contains a value from the <a href="https://msdn.microsoft.com/682fa0c7-8f17-457f-9f8a-dc9190866152">DXVA2_VideoTransferMatrix</a> enumeration.


### -field VideoLighting

Describes the intended viewing conditions. Contains a value from the <a href="https://msdn.microsoft.com/d70e7aa7-f68f-4ee3-bb75-dbe369e68f0e">DXVA2_VideoLighting</a> enumeration.


### -field VideoPrimaries

Describes the color primaries. Contains a value from the <a href="https://msdn.microsoft.com/4534a198-cf6c-4689-9fe4-0e5cdc7ce26a">DXVA2_VideoPrimaries</a> enumeration.


### -field VideoTransferFunction

Describes the gamma correction transfer function. Contains a value from the <a href="https://msdn.microsoft.com/43b99d5f-ea28-4de2-b118-e2277f283dee">DXVA2_VideoTransferFunction</a> enumeration.


### -field value

Use this member to access all of the bits in the union.


## -remarks



Most of the values in this structure can be translated directly to and from <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> attributes. For a code example that fills in the values from an <b>IMFMediaType</b> pointer, see <a href="https://msdn.microsoft.com/0e500a08-a3b5-475c-8bbc-e4b30cce247d">DXVA2_VideoDesc</a>.




## -see-also




<a href="https://msdn.microsoft.com/05ca73c6-d105-47bc-96bc-b784f669febe">Extended Color Information</a>



<a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

