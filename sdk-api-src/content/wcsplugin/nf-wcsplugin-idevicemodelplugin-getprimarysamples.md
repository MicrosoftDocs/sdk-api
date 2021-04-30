---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetPrimarySamples
title: IDeviceModelPlugIn::GetPrimarySamples (wcsplugin.h)
description: Returns the measurement color for the primary sample.
helpviewer_keywords: ["GetPrimarySamples","GetPrimarySamples method [Windows Color System]","GetPrimarySamples method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","GetPrimarySamples method","IDeviceModelPlugIn.GetPrimarySamples","IDeviceModelPlugIn::GetPrimarySamples","_color_IDeviceModelPlugIn::GetPrimarySamples","wcs.IDeviceModelPlugIn_GetPrimarySamples","wcsplugin/IDeviceModelPlugIn::GetPrimarySamples"]
old-location: wcs\IDeviceModelPlugIn_GetPrimarySamples.htm
tech.root: WCS
ms.assetid: 46253246-e07c-4f55-92fa-91941abaefcd
ms.date: 12/05/2018
ms.keywords: GetPrimarySamples, GetPrimarySamples method [Windows Color System], GetPrimarySamples method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetPrimarySamples method, IDeviceModelPlugIn.GetPrimarySamples, IDeviceModelPlugIn::GetPrimarySamples, _color_IDeviceModelPlugIn::GetPrimarySamples, wcs.IDeviceModelPlugIn_GetPrimarySamples, wcsplugin/IDeviceModelPlugIn::GetPrimarySamples
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
 - IDeviceModelPlugIn::GetPrimarySamples
 - wcsplugin/IDeviceModelPlugIn::GetPrimarySamples
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
 - IDeviceModelPlugIn.GetPrimarySamples
---

# IDeviceModelPlugIn::GetPrimarySamples


## -description

Returns the measurement color for the primary sample.

## -parameters

### -param pPrimaryColor [out]

The primary color type, which is determined by using the hue circle order. If the plugin device model does not natively support primaries for red, yellow, green, cyan, blue, magenta, black and white, it must still return virtual primary data.

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)
