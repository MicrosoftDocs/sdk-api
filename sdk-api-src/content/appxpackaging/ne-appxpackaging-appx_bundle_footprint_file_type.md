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

# APPX_BUNDLE_FOOTPRINT_FILE_TYPE enumeration


## -description


Specifies the type of footprint file in a bundle. 


## -enum-fields




### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_FIRST

The bundle's first footprint file, which is the bundle manifest. 


### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_MANIFEST

The bundle manifest.


### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_BLOCKMAP

The bundle block map.


### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_SIGNATURE

The bundle signature. 


### -field APPX_BUNDLE_FOOTPRINT_FILE_TYPE_LAST

The bundle's last footprint file, which is the bundle signature. 


## -see-also




<a href="https://msdn.microsoft.com/BD60CD3E-2C08-4B97-B311-00C0EEBEF752">IAppxBundleReader::GetFootprintFile</a>
 

 

