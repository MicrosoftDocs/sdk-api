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

# APPX_FOOTPRINT_FILE_TYPE enumeration


## -description


Specifies the type of footprint file in a package.


## -enum-fields




### -field APPX_FOOTPRINT_FILE_TYPE_MANIFEST

The package manifest.


### -field APPX_FOOTPRINT_FILE_TYPE_BLOCKMAP

The package block map.


### -field APPX_FOOTPRINT_FILE_TYPE_SIGNATURE

The package signature.


### -field APPX_FOOTPRINT_FILE_TYPE_CODEINTEGRITY

The code signing catalog file used for code integrity checks.


### -field APPX_FOOTPRINT_FILE_TYPE_CONTENTGROUPMAP

The content group map used for streaming install.


## -see-also




<a href="https://msdn.microsoft.com/8CCF9135-308F-4BDC-A67F-1E3ED2ACF565">IAppxPackageReader::GetFootprintFile</a>
 

 

