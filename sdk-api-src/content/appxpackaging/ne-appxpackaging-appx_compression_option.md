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

# APPX_COMPRESSION_OPTION enumeration


## -description


Specifies the degree of compression used to store the file in the package.


## -enum-fields




### -field APPX_COMPRESSION_OPTION_NONE

No compression.


### -field APPX_COMPRESSION_OPTION_NORMAL

Normal  compression.


### -field APPX_COMPRESSION_OPTION_MAXIMUM

Maximum compression.


### -field APPX_COMPRESSION_OPTION_FAST

Fast compression.


### -field APPX_COMPRESSION_OPTION_SUPERFAST

Super-fast compression.


## -see-also




<a href="https://msdn.microsoft.com/E2F33ED4-EAD3-44AE-B646-3AB875FA7606">IAppxFile::GetCompressionOption</a>



<a href="https://msdn.microsoft.com/2BFC725A-CD56-46CA-983A-FD1BFB6CB474">IAppxPackageWriter::AddPayloadFile</a>
 

 

