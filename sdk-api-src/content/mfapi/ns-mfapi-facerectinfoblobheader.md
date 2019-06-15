---
UID: NS:mfapi.tagFaceRectInfoBlobHeader
title: FaceRectInfoBlobHeader (mfapi.h)
author: windows-sdk-content
description: The FaceRectInfoBlobHeader structure describes the size and count information of the blob format for the MF_CAPTURE_METADATA_FACEROIS attribute.
old-location: stream\facerectinfoblobheader.htm
tech.root: stream
ms.assetid: BDDC33C2-CD2D-4F97-AAD1-DF69250F60B3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FaceRectInfoBlobHeader, FaceRectInfoBlobHeader structure [Streaming Media Devices], mfapi/FaceRectInfoBlobHeader, stream.facerectinfoblobheader
ms.topic: struct
f1_keywords: ["mfapi/FaceRectInfoBlobHeader"]
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
 - FaceRectInfoBlobHeader
product: Windows
targetos: Windows
req.typenames: FaceRectInfoBlobHeader
req.redist: 
ms.custom: 19H1
---

# FaceRectInfoBlobHeader structure


## -description


The <b>FaceRectInfoBlobHeader</b> structure describes the size and count information of the blob format for the <b>MF_CAPTURE_METADATA_FACEROIS</b> attribute.


## -struct-fields




### -field Size

Size of this header + all following <a href="https://docs.microsoft.com/windows/desktop/api/mfapi/ns-mfapi-tagfacerectinfo">FaceRectInfo</a> structures.


### -field Count

Number of <b>FaceRectInfo</b> structures in the blob.

