---
UID: NE:d2d1_3.D2D1_IMAGE_SOURCE_LOADING_OPTIONS
title: D2D1_IMAGE_SOURCE_LOADING_OPTIONS (d2d1_3.h)
author: windows-sdk-content
description: Controls option flags for a new ID2D1ImageSource when it is created.
old-location: direct2d\D2D1_IMAGE_SOURCE_LOADING_OPTIONS.htm
tech.root: Direct2D
ms.assetid: b2dcd7aa-177c-62bf-cb3e-2eb4bd4f9627
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D2D1_IMAGE_SOURCE_LOADING_OPTIONS, D2D1_IMAGE_SOURCE_LOADING_OPTIONS enumeration [Direct2D], D2D1_IMAGE_SOURCE_LOADING_OPTIONS_CACHE_ON_DEMAND, D2D1_IMAGE_SOURCE_LOADING_OPTIONS_NONE, D2D1_IMAGE_SOURCE_LOADING_OPTIONS_RELEASE_SOURCE, d2d1_3/D2D1_IMAGE_SOURCE_LOADING_OPTIONS, d2d1_3/D2D1_IMAGE_SOURCE_LOADING_OPTIONS_CACHE_ON_DEMAND, d2d1_3/D2D1_IMAGE_SOURCE_LOADING_OPTIONS_NONE, d2d1_3/D2D1_IMAGE_SOURCE_LOADING_OPTIONS_RELEASE_SOURCE, direct2d.D2D1_IMAGE_SOURCE_LOADING_OPTIONS
ms.topic: enum
f1_keywords: 
 - "d2d1_3/D2D1_IMAGE_SOURCE_LOADING_OPTIONS"
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - d2d1_3.h
api_name:
 - D2D1_IMAGE_SOURCE_LOADING_OPTIONS
product: Windows
targetos: Windows
req.typenames: D2D1_IMAGE_SOURCE_LOADING_OPTIONS
req.redist: 
ms.custom: 19H1
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
        the <a href="https://docs.microsoft.com/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1imagesourcefromwic-ensurecached(constd2d1_rect_u)">EnsureCached</a> 
          and <a href="https://docs.microsoft.com/windows/win32/api/d2d1_3/nf-d2d1_3-id2d1imagesourcefromwic-trimcache">TrimCache</a> methods. 
        This options provides the ability to improve memory usage by only keeping needed portions of the image in memory. 
        This option requires that the image source has a reference to the WIC bitmap source, and is incompatible with D2D1_IMAGE_SOURCE_LOADING_OPTIONS_RELEASE_SOURCE.


### -field D2D1_IMAGE_SOURCE_LOADING_OPTIONS_FORCE_DWORD




## -remarks



D2D1_IMAGE_SOURCE_CREATION_OPTIONS_RELEASE_SOURCE causes the image source to not retain a reference to the source object used to create it.  
      It can decrease the quality and efficiency of printing.



