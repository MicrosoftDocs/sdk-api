---
UID: NE:codecapi.eAVDecVideoInputScanType
title: eAVDecVideoInputScanType
author: windows-sdk-content
description: Specifies how the decoded video stream is interlaced. This enumeration is used with the AVDecVideoInputScanType property.
old-location: dshow\eavdecvideoinputscantype.htm
tech.root: DirectShow
ms.assetid: 9ea17960-af08-42ba-9646-7aaf498ceda1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: codecapi/eAVDecVideoInputScanType, codecapi/eAVDecVideoInputScan_Interlaced_LowerFieldFirst, codecapi/eAVDecVideoInputScan_Interlaced_UpperFieldFirst, codecapi/eAVDecVideoInputScan_Progressive, codecapi/eAVDecVideoInputScan_Unknown, dshow.eavdecvideoinputscantype, eAVDecVideoInputScanType, eAVDecVideoInputScanType enumeration [DirectShow], eAVDecVideoInputScanTypeEnumeration, eAVDecVideoInputScan_Interlaced_LowerFieldFirst, eAVDecVideoInputScan_Interlaced_UpperFieldFirst, eAVDecVideoInputScan_Progressive, eAVDecVideoInputScan_Unknown
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
 - eAVDecVideoInputScanType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVDecVideoInputScanType enumeration


## -description



Specifies how the decoded video stream is interlaced. This enumeration is used with the <a href="https://msdn.microsoft.com/a2b95b90-1c58-47f3-b6a8-0f3f6f1a416c">AVDecVideoInputScanType</a> property.




## -enum-fields




### -field eAVDecVideoInputScan_Unknown

The interlacing is not known.


### -field eAVDecVideoInputScan_Progressive

Decoded frames are progressive.


### -field eAVDecVideoInputScan_Interlaced_UpperFieldFirst

Decoded frames are interlaced, with the upper field appearing first.


### -field eAVDecVideoInputScan_Interlaced_LowerFieldFirst

Decoded frames are interlaced, with the lower field appearing first.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

