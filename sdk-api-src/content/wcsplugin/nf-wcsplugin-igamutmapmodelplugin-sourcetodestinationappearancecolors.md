---
UID: NF:wcsplugin.IGamutMapModelPlugIn.SourceToDestinationAppearanceColors
title: IGamutMapModelPlugIn::SourceToDestinationAppearanceColors
author: windows-sdk-content
description: Returns the appropriate gamut-mapped appearance colors in response to the specified number of colors and the CIEJCh colors.
old-location: wcs\IGamutMapModelPlugIn_SourceToDestinationAppearanceColors.htm
old-project: WCS
ms.assetid: b98f05db-f003-4a3f-9bc3-0675719e339d
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: IGamutMapModelPlugIn interface [Windows Color System],SourceToDestinationAppearanceColors method, IGamutMapModelPlugIn.SourceToDestinationAppearanceColors, IGamutMapModelPlugIn::SourceToDestinationAppearanceColors, SourceToDestinationAppearanceColors, SourceToDestinationAppearanceColors method [Windows Color System], SourceToDestinationAppearanceColors method [Windows Color System],IGamutMapModelPlugIn interface, _color_IGamutMapModelPlugIn::SourceToDestinationAppearanceColors, wcs.IGamutMapModelPlugIn_SourceToDestinationAppearanceColors, wcsplugin/IGamutMapModelPlugIn::SourceToDestinationAppearanceColors
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcsplugin.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WCN_VALUE_TYPE_PRIMARY_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcsPlugIn.h
api_name:
 - IGamutMapModelPlugIn.SourceToDestinationAppearanceColors
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IGamutMapModelPlugIn::SourceToDestinationAppearanceColors


## -description


Returns the appropriate gamut-mapped appearance colors in response to the specified number of colors and the <a href="wcs.IGamutMapModelPlugIn::SourceToDestinationAppearanceColors">CIEJCh</a> colors.


## -parameters




### -param cColors [in]

The number of colors in the <i>pXYZColors</i> and <i>pDeviceValues</i> arrays.


### -param pInputColors [in]

A pointer to the array of incoming colors to be gamut mapped.


### -param pOutputColors [out]

A pointer to the array of outgoing colors.


## -returns



If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/794eb94c-fdb3-42b3-8320-b13bf51324d1">IGamutMapModelPlugIn</a>
 

 

