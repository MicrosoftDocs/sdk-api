---
UID: NS:wcsplugin._GamutBoundaryDescription
title: GamutBoundaryDescription
author: windows-sdk-content
description: Defines a gamut boundary.
old-location: wcs\gamutboundarydescription.htm
tech.root: WCS
ms.assetid: b7551967-ff2f-48ed-9346-a75e19fe2c31
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GamutBoundaryDescription, GamutBoundaryDescription structure [Windows Color System], _color_GamutBoundaryDescription_str, wcs.gamutboundarydescription, wcsplugin/GamutBoundaryDescription
ms.topic: struct
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




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/68d681e6-4798-449b-9afd-ab35f24d6e67">Structures</a>



<a href="https://msdn.microsoft.com/fa05ba0c-b01d-4d50-8769-94a6e19f0066">Windows Color System Schemas and Algorithms</a>
 

 

