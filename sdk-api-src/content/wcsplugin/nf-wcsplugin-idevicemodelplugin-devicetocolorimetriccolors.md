---
UID: NF:wcsplugin.IDeviceModelPlugIn.DeviceToColorimetricColors
title: IDeviceModelPlugIn::DeviceToColorimetricColors (wcsplugin.h)
description: Returns the appropriate XYZ colors in response to the specified number of colors, channels, device colors and the proprietary plug-in algorithms. (IDeviceModelPlugIn.DeviceToColorimetricColors)
helpviewer_keywords: ["DeviceToColorimetricColors","DeviceToColorimetricColors method [Windows Color System]","DeviceToColorimetricColors method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","DeviceToColorimetricColors method","IDeviceModelPlugIn.DeviceToColorimetricColors","IDeviceModelPlugIn::DeviceToColorimetricColors","_color_IDeviceModelPlugIn::DeviceToColorimetricColors","wcs.IDeviceModelPlugIn_DeviceToColorimetricColors","wcsplugin/IDeviceModelPlugIn::DeviceToColorimetricColors"]
old-location: wcs\IDeviceModelPlugIn_DeviceToColorimetricColors.htm
tech.root: WCS
ms.assetid: 828961e6-c0b6-4622-8edb-15854daf6ae9
ms.date: 12/05/2018
ms.keywords: DeviceToColorimetricColors, DeviceToColorimetricColors method [Windows Color System], DeviceToColorimetricColors method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],DeviceToColorimetricColors method, IDeviceModelPlugIn.DeviceToColorimetricColors, IDeviceModelPlugIn::DeviceToColorimetricColors, _color_IDeviceModelPlugIn::DeviceToColorimetricColors, wcs.IDeviceModelPlugIn_DeviceToColorimetricColors, wcsplugin/IDeviceModelPlugIn::DeviceToColorimetricColors
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
 - IDeviceModelPlugIn::DeviceToColorimetricColors
 - wcsplugin/IDeviceModelPlugIn::DeviceToColorimetricColors
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
 - IDeviceModelPlugIn.DeviceToColorimetricColors
---

# IDeviceModelPlugIn::DeviceToColorimetricColors


## -description

Returns the appropriate XYZ colors in response to the specified number of colors, channels, device colors and the proprietary plug-in algorithms.

## -parameters

### -param cColors [in]

The number of colors in the <i>pXYZColors</i> and <i>pDeviceValues</i> arrays.

### -param cChannels [in]

The number of color channels in the <i>pDeviceValues</i> arrays.

### -param pDeviceValues [in]

A pointer to the array of outgoing XYZColors.

### -param pXYZColors [out]

A pointer to the array of incoming device colors to convert to XYZColors.

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL. For extended error information, call <b>GetLastError</b>.

## -remarks

If <i>cColors</i> or <i>cChannels</i> is zero, the return value is E_FAIL.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)
