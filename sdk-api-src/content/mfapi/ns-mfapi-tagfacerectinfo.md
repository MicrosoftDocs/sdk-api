---
UID: NS:mfapi.tagFaceRectInfo
title: tagFaceRectInfo
author: windows-sdk-content
description: The FaceRectInfo structure describes the blob format for the MF_CAPTURE_METADATA_FACEROIS attribute.
old-location: stream\facerectinfo.htm
tech.root: stream
ms.assetid: 63F31CDC-CB44-4ED8-BDA0-89F7DCF77965
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: FaceRectInfo, FaceRectInfo structure [Streaming Media Devices], mfapi/FaceRectInfo, stream.facerectinfo, tagFaceRectInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mfapi.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfapi.h
api_name:
 - FaceRectInfo
product: Windows
targetos: Windows
req.typenames: FaceRectInfo
req.redist: 
---

# tagFaceRectInfo structure


## -description


The <b>FaceRectInfo</b> structure describes the blob format for the <b>MF_CAPTURE_METADATA_FACEROIS</b> attribute.


## -struct-fields




### -field Region

Relative coordinates on the frame that face detection is running (Q31 format).


### -field confidenceLevel

 




#### - ConfidenceLevel

Confidence level of the region being a face (0 - 100).


## -remarks



The <b>MF_CAPTURE_METADATA_FACEROIS</b> attribute contains the face rectangle info detected by the driver.   By default driver\MFT0 should provide the face information on preview stream.  If the driver advertises the capability on other streams, driver\MFT must provide the face info on the corresponding streams if the application enables face detection on those streams.  When video stabilization is enabled on the driver, the face information should be provided post-video stabilization. The dominate face must be the first <b>FaceRectInfo</b> in the blob.

The <a href="https://msdn.microsoft.com/BDDC33C2-CD2D-4F97-AAD1-DF69250F60B3">FaceRectInfoBlobHeader</a> and <b>FaceRectInfo</b> structures only describe the blob format for the <b>MF_CAPTURE_METADATA_FACEROIS</b> attribute.  The metadata item structure for face ROIs (<a href="https://msdn.microsoft.com/B4AC04D7-9F98-41F1-A38D-927F3F3A7699">KSCAMERA_METADATA_ITEMHEADER</a> + face ROIs metadata payload) is up to driver and must be 8-byte aligned.



