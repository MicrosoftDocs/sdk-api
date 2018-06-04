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

# D2D1_IMAGE_SOURCE_LOADING_OPTIONS enumeration


## -description


Controls option flags for a new ID2D1ImageSource when it is created.


## -enum-fields




### -field D2D1_IMAGE_SOURCE_LOADING_OPTIONS_NONE

No options are used.


### -field D2D1_IMAGE_SOURCE_LOADING_OPTIONS_RELEASE_SOURCE

Indicates the image source should release its reference to the WIC bitmap source after it has initialized. 
        By default, the image source retains a reference to the WIC bitmap source for the lifetime of the object to enable quality and speed optimizations for printing. 
        This option disables that optimization.



### -field D2D1_IMAGE_SOURCE_LOADING_OPTIONS_CACHE_ON_DEMAND

Indicates the image source should only populate subregions of the image cache on-demand. You can control this behavior using 
        the <a href="https://msdn.microsoft.com/9addc82b-7446-1f2c-5666-f817b8b5707d">EnsureCached</a> 
          and <a href="https://msdn.microsoft.com/04e6e010-3642-6775-8a95-f20ff0461b09">TrimCache</a> methods. 
        This options provides the ability to improve memory usage by only keeping needed portions of the image in memory. 
        This option requires that the image source has a reference to the WIC bitmap source, and is incompatible with D2D1_IMAGE_SOURCE_LOADING_OPTIONS_RELEASE_SOURCE.


### -field D2D1_IMAGE_SOURCE_LOADING_OPTIONS_FORCE_DWORD




## -remarks




 
      

D2D1_IMAGE_SOURCE_CREATION_OPTIONS_RELEASE_SOURCE causes the image source to not retain a reference to the source object used to create it.  
      It can decrease the quality and efficiency of printing.



