---
UID: NF:wcsplugin.IGamutMapModelPlugIn.SourceToDestinationAppearanceColors
title: IGamutMapModelPlugIn::SourceToDestinationAppearanceColors (wcsplugin.h)
description: Returns the appropriate gamut-mapped appearance colors in response to the specified number of colors and the CIEJCh colors.
helpviewer_keywords: ["IGamutMapModelPlugIn interface [Windows Color System]","SourceToDestinationAppearanceColors method","IGamutMapModelPlugIn.SourceToDestinationAppearanceColors","IGamutMapModelPlugIn::SourceToDestinationAppearanceColors","SourceToDestinationAppearanceColors","SourceToDestinationAppearanceColors method [Windows Color System]","SourceToDestinationAppearanceColors method [Windows Color System]","IGamutMapModelPlugIn interface","_color_IGamutMapModelPlugIn::SourceToDestinationAppearanceColors","wcs.IGamutMapModelPlugIn_SourceToDestinationAppearanceColors","wcsplugin/IGamutMapModelPlugIn::SourceToDestinationAppearanceColors"]
old-location: wcs\IGamutMapModelPlugIn_SourceToDestinationAppearanceColors.htm
tech.root: WCS
ms.assetid: b98f05db-f003-4a3f-9bc3-0675719e339d
ms.date: 12/05/2018
ms.keywords: IGamutMapModelPlugIn interface [Windows Color System],SourceToDestinationAppearanceColors method, IGamutMapModelPlugIn.SourceToDestinationAppearanceColors, IGamutMapModelPlugIn::SourceToDestinationAppearanceColors, SourceToDestinationAppearanceColors, SourceToDestinationAppearanceColors method [Windows Color System], SourceToDestinationAppearanceColors method [Windows Color System],IGamutMapModelPlugIn interface, _color_IGamutMapModelPlugIn::SourceToDestinationAppearanceColors, wcs.IGamutMapModelPlugIn_SourceToDestinationAppearanceColors, wcsplugin/IGamutMapModelPlugIn::SourceToDestinationAppearanceColors
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGamutMapModelPlugIn::SourceToDestinationAppearanceColors
 - wcsplugin/IGamutMapModelPlugIn::SourceToDestinationAppearanceColors
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcsPlugIn.h
api_name:
 - IGamutMapModelPlugIn.SourceToDestinationAppearanceColors
---

# IGamutMapModelPlugIn::SourceToDestinationAppearanceColors


## -description

Returns the appropriate gamut-mapped appearance colors in response to the specified number of colors and the <a href="/windows/win32/api/_wcs/">CIEJCh</a> colors.

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

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [IGamutMapModelPlugIn](/windows/win32/api/wcsplugin/nn-wcsplugin-igamutmapmodelplugin)
