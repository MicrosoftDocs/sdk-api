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

# WICJpegYCrCbSubsamplingOption enumeration


## -description


Specifies the JPEG YCrCB subsampling options. 


## -enum-fields




### -field WICJpegYCrCbSubsamplingDefault

The default subsampling option. 


### -field WICJpegYCrCbSubsampling420

Subsampling option that uses both horizontal and vertical decimation.


### -field WICJpegYCrCbSubsampling422

Subsampling option that uses horizontal decimation  .


### -field WICJpegYCrCbSubsampling444

Subsampling option that uses no decimation.


### -field WICJpegYCrCbSubsampling440

Subsampling option that uses 2x vertical downsampling only. This option is only available in Windows 8.1 and later.


### -field WICJPEGYCRCBSUBSAMPLING_FORCE_DWORD




## -remarks



The native JPEG encoder uses <b>WICJpegYCrCbSubsampling420</b>.



