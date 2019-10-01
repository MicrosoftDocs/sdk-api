---
UID: NS:mfapi.tagFaceCharacterizationBlobHeader
title: FaceCharacterizationBlobHeader (mfapi.h)
author: windows-sdk-content
description: The FaceCharacterizationBlobHeader structure describes the size and count information of the blob format for the MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS attribute.
old-location: stream\facecharacterizationblobheader.htm
tech.root: stream
ms.assetid: F3BDB935-A8CB-41BA-B912-0B9264FE0B09
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FaceCharacterizationBlobHeader, FaceCharacterizationBlobHeader structure [Streaming Media Devices], mfapi/FaceCharacterizationBlobHeader, stream.facecharacterizationblobheader
ms.topic: struct
f1_keywords: 
 - "mfapi/FaceCharacterizationBlobHeader"
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
targetos: Windows
req.typenames: FaceCharacterizationBlobHeader
req.redist: 
ms.custom: 19H1
---

# FaceCharacterizationBlobHeader structure


## -description


The <b>FaceCharacterizationBlobHeader</b> structure  describes the size and count information of the blob format for the <b>MF_CAPTURE_METADATA_FACEROICHARACTERIZATIONS</b> attribute.


## -struct-fields




### -field Size

Size of this header + all following <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/ns-mfapi-facecharacterization">FaceCharacterization</a> structures.


### -field Count

Number of <b>FaceCharacterization</b> structures in the blob. Must match the number of <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/ns-mfapi-facerectinfo">FaceRectInfo</a> structures in <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/ns-mfapi-facerectinfoblobheader">FaceRectInfoBlobHeader</a>.

