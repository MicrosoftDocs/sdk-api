---
UID: NS:icm.tagNAMED_PROFILE_INFO
title: tagNAMED_PROFILE_INFO
author: windows-sdk-content
description: The NAMED_PROFILE_INFO structure is used to store information about a named color profile.
old-location: wcs\named_profile_info.htm
tech.root: WCS
ms.assetid: decb0b76-872c-4237-a2b0-6da83d49c8cf
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: "*PNAMED_PROFILE_INFO, NAMED_PROFILE_INFO, NAMED_PROFILE_INFO structure [Windows Color System], _color_NAMED_PROFILE_INFO_str, icm/NAMED_PROFILE_INFO, tagNAMED_PROFILE_INFO, wcs.named_profile_info"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: icm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Icm.h
api_name:
 - NAMED_PROFILE_INFO
product: Windows
targetos: Windows
req.typenames: NAMED_PROFILE_INFO
req.redist: 
---

# tagNAMED_PROFILE_INFO structure


## -description



The <b>NAMED_PROFILE_INFO</b> structure is used to store information about a named color profile.




## -struct-fields




### -field dwFlags

Not currently used by the default CMM.


### -field dwCount

Total number of named colors in the profile.


### -field dwCountDevCoordinates

Total number of device coordinates for each named color.


### -field szPrefix

Pointer to a string containing the prefix for each color name.


### -field szSuffix

Pointer to a string containing the suffix for each color name.

