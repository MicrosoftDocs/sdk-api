---
UID: NS:mfobjects._MFVideoCompressedInfo
title: "_MFVideoCompressedInfo"
author: windows-sdk-content
description: Contains information about a video compression format. This structure is used in the MFVIDEOFORMAT structure.
old-location: mf\mfvideocompressedinfo.htm
tech.root: medfound
ms.assetid: fe9aa287-33e9-4413-8bc5-0e7b2da1112e
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: MFVideoCompressedInfo, MFVideoCompressedInfo structure [Media Foundation], _MFVideoCompressedInfo, fe9aa287-33e9-4413-8bc5-0e7b2da1112e, mf.mfvideocompressedinfo, mfobjects/MFVideoCompressedInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
 - MFVideoCompressedInfo
product: Windows
targetos: Windows
req.typenames: MFVideoCompressedInfo
req.redist: 
---

# _MFVideoCompressedInfo structure


## -description



Contains information about a video compression format. This structure is used in the <a href="https://msdn.microsoft.com/7fbc4a35-117c-4f0c-9e9b-ff44e30a1618">MFVIDEOFORMAT</a> structure.




## -struct-fields




### -field AvgBitrate

Average bit rate of the encoded video stream, in bits per second.


### -field AvgBitErrorRate

Expected error rate, in bits per second.


### -field MaxKeyFrameSpacing

Number of frames between key frames.


## -remarks



For uncompressed video formats, set the structure members to zero.




## -see-also




<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>



<a href="https://msdn.microsoft.com/690fda6e-dcbd-44dc-968d-cc949126da81">Media Types</a>
 

 

