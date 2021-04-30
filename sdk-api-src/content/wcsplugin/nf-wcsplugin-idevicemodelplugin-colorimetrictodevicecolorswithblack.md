---
UID: NF:wcsplugin.IDeviceModelPlugIn.ColorimetricToDeviceColorsWithBlack
title: IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack (wcsplugin.h)
description: Returns the appropriate device colors in response to the incoming number of colors, channels, black information, Commission Internationale l'Eclairge XYZ (CIEXYZ) colors and the proprietary plug-in algorithms.
helpviewer_keywords: ["ColorimetricToDeviceColorsWithBlack","ColorimetricToDeviceColorsWithBlack method [Windows Color System]","ColorimetricToDeviceColorsWithBlack method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","ColorimetricToDeviceColorsWithBlack method","IDeviceModelPlugIn.ColorimetricToDeviceColorsWithBlack","IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack","_color_IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack","wcs.IDeviceModelPlugIn_ColorimetricToDeviceColorsWithBlack","wcsplugin/IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack"]
old-location: wcs\IDeviceModelPlugIn_ColorimetricToDeviceColorsWithBlack.htm
tech.root: WCS
ms.assetid: 74ec9ace-2468-4b26-a419-781f0b4fd073
ms.date: 12/05/2018
ms.keywords: ColorimetricToDeviceColorsWithBlack, ColorimetricToDeviceColorsWithBlack method [Windows Color System], ColorimetricToDeviceColorsWithBlack method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],ColorimetricToDeviceColorsWithBlack method, IDeviceModelPlugIn.ColorimetricToDeviceColorsWithBlack, IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack, _color_IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack, wcs.IDeviceModelPlugIn_ColorimetricToDeviceColorsWithBlack, wcsplugin/IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack
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
 - IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack
 - wcsplugin/IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack
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
 - IDeviceModelPlugIn.ColorimetricToDeviceColorsWithBlack
---

# IDeviceModelPlugIn::ColorimetricToDeviceColorsWithBlack


## -description

Returns the appropriate device colors in response to the incoming number of colors, channels, black information, Commission Internationale l'Eclairge XYZ (CIEXYZ) colors and the proprietary plug-in algorithms.

## -parameters

### -param cColors [in]

The number of colors in the <i>pXYZColors</i> and <i>pDeviceValues</i> arrays.

### -param cChannels [in]

The number of color channels in the <i>pDeviceValues</i> arrays.

### -param pXYZColors [out]

A pointer to the array of outgoing <a href="/windows/win32/api/wcsplugin/ns-wcsplugin-xyzcolorf">XYZColorF</a> structures.

### -param pBlackInformation [in]

A pointer to the <a href="/windows/desktop/api/wcsplugin/ns-wcsplugin-blackinformation">BlackInformation</a>.

### -param pDeviceValues [in]

A pointer to the array of incoming device colors that are to be converted to <a href="/windows/win32/api/wcsplugin/ns-wcsplugin-xyzcolorf">XYZColorF</a> structures.

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL. For extended error information, call <b>GetLastError</b>.

## -remarks

If <i>cColors</i> or <i>cChannels</i> is zero, the return value is E_FAIL.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)
