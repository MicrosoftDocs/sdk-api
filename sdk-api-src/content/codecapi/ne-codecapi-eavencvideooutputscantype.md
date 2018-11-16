---
UID: NE:codecapi.eAVEncVideoOutputScanType
title: eAVEncVideoOutputScanType
author: windows-sdk-content
description: Specifies how the encoder interlaces the output video. This enumeration is used with the AVEncVideoOutputScanType property.
old-location: dshow\eavencvideooutputscantype.htm
tech.root: DirectShow
ms.assetid: 95389593-ce88-4f23-ae87-ff1cb67c2e8c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: codecapi/eAVEncVideoOutputScanType, codecapi/eAVEncVideoOutputScan_Automatic, codecapi/eAVEncVideoOutputScan_Interlaced, codecapi/eAVEncVideoOutputScan_Progressive, codecapi/eAVEncVideoOutputScan_SameAsInput, dshow.eavencvideooutputscantype, eAVEncVideoOutputScanType, eAVEncVideoOutputScanType enumeration [DirectShow], eAVEncVideoOutputScanTypeEnumeration, eAVEncVideoOutputScan_Automatic, eAVEncVideoOutputScan_Interlaced, eAVEncVideoOutputScan_Progressive, eAVEncVideoOutputScan_SameAsInput
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - codecapi.h
api_name:
 - eAVEncVideoOutputScanType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVEncVideoOutputScanType enumeration


## -description



Specifies how the encoder interlaces the output video. This enumeration is used with the <a href="https://msdn.microsoft.com/f36238dc-2152-4faf-835e-1027ef1af73b">AVEncVideoOutputScanType</a> property.




## -enum-fields




### -field eAVEncVideoOutputScan_Progressive

Output frames are progressive.


### -field eAVEncVideoOutputScan_Interlaced

Output frames are interlaced.


### -field eAVEncVideoOutputScan_SameAsInput

The interlacing on the output frames matches the input frames.


### -field eAVEncVideoOutputScan_Automatic

Use the media type on the encoder's input pin to determine whether the frames are progressive or interlaced.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

