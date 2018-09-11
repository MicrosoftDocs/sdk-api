---
UID: NS:mfapi.tagFaceCharacterizationBlobHeader
title: tagFaceCharacterizationBlobHeader
author: windows-sdk-content
description: The FaceCharacterizationBlobHeader structure describes the size and count information of the blob format for the MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS attribute.
old-location: stream\facecharacterizationblobheader.htm
tech.root: stream
ms.assetid: F3BDB935-A8CB-41BA-B912-0B9264FE0B09
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: FaceCharacterizationBlobHeader, FaceCharacterizationBlobHeader structure [Streaming Media Devices], mfapi/FaceCharacterizationBlobHeader, stream.facecharacterizationblobheader, tagFaceCharacterizationBlobHeader
ms.prod: windows
ms.technology: windows-sdk
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
 - FaceCharacterizationBlobHeader
product: Windows
targetos: Windows
req.typenames: FaceCharacterizationBlobHeader
req.redist: 
---

# tagFaceCharacterizationBlobHeader structure


## -description


The <b>FaceCharacterizationBlobHeader</b> structure  describes the size and count information of the blob format for the <b>MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS</b> attribute.


## -struct-fields




### -field Size

Size of this header + all following <a href="https://msdn.microsoft.com/8A8F6E06-DA09-4595-BF42-8B905453CCCA">FaceCharacterization</a> structures.


### -field Count

Number of <b>FaceCharacterization</b> structures in the blob. Must match the number of <a href="https://msdn.microsoft.com/63F31CDC-CB44-4ED8-BDA0-89F7DCF77965">FaceRectInfo</a> structures in <a href="https://msdn.microsoft.com/BDDC33C2-CD2D-4F97-AAD1-DF69250F60B3">FaceRectInfoBlobHeader</a>.

