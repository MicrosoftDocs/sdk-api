---
UID: NF:wcsplugin.IDeviceModelPlugIn.DeviceToColorimetricColors
title: IDeviceModelPlugIn::DeviceToColorimetricColors (wcsplugin.h)
description: Returns the appropriate XYZ colors in response to the specified number of colors, channels, device colors and the proprietary plug-in algorithms.
helpviewer_keywords: ["DeviceToColorimetricColors","DeviceToColorimetricColors method [Windows Color System]","DeviceToColorimetricColors method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","DeviceToColorimetricColors method","IDeviceModelPlugIn.DeviceToColorimetricColors","IDeviceModelPlugIn::DeviceToColorimetricColors","_color_IDeviceModelPlugIn::DeviceToColorimetricColors","wcs.IDeviceModelPlugIn_DeviceToColorimetricColors","wcsplugin/IDeviceModelPlugIn::DeviceToColorimetricColors"]
old-location: wcs\IDeviceModelPlugIn_DeviceToColorimetricColors.htm
tech.root: WCS
ms.assetid: 828961e6-c0b6-4622-8edb-15854daf6ae9
ms.date: 12/05/2018
ms.keywords: DeviceToColorimetricColors, DeviceToColorimetricColors method [Windows Color System], DeviceToColorimetricColors method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],DeviceToColorimetricColors method, IDeviceModelPlugIn.DeviceToColorimetricColors, IDeviceModelPlugIn::DeviceToColorimetricColors, _color_IDeviceModelPlugIn::DeviceToColorimetricColors, wcs.IDeviceModelPlugIn_DeviceToColorimetricColors, wcsplugin/IDeviceModelPlugIn::DeviceToColorimetricColors
f1_keywords:
- wcsplugin/IDeviceModelPlugIn.DeviceToColorimetricColors
dev_langs:
- c++
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
- COM
api_location:
- WcsPlugIn.h
api_name:
- IDeviceModelPlugIn.DeviceToColorimetricColors
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin">IDeviceModelPlugIn</a>
 

 

