---
UID: NS:wcsplugin._GamutBoundaryDescription
title: GamutBoundaryDescription (wcsplugin.h)
author: windows-sdk-content
description: Defines a gamut boundary.
old-location: wcs\gamutboundarydescription.htm
tech.root: WCS
ms.assetid: b7551967-ff2f-48ed-9346-a75e19fe2c31
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GamutBoundaryDescription, GamutBoundaryDescription structure [Windows Color System], _color_GamutBoundaryDescription_str, wcs.gamutboundarydescription, wcsplugin/GamutBoundaryDescription
ms.topic: struct
f1_keywords: ["wcsplugin/GamutBoundaryDescription"]
req.header: wcsplugin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WcsPlugIn.h
api_name:
 - GamutBoundaryDescription
product: Windows
targetos: Windows
req.typenames: GamutBoundaryDescription
req.redist: 
ms.custom: 19H1
---

# GamutBoundaryDescription structure


## -description



Defines a gamut boundary.




## -struct-fields




### -field pPrimaries

 


### -field cNeutralSamples

The number of neutral samples.


### -field pNeutralSamples

 


### -field pReferenceShell

 


### -field pPlausibleShell

 


### -field pPossibleShell

 




#### - *pNeutralSamples

A pointer to the neutral samples.


#### - *pPlausibleShell

A pointer to the plausible shell.


#### - *pPossibleShell

A pointer to the possible shell.


#### - *pReferenceShell

A pointer to the reference shell.


#### - primaries

The primary colors.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/structures">Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/windows-color-system-schemas-and-algorithms">Windows Color System Schemas and Algorithms</a>
 

 

