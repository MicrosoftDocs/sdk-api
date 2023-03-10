---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetNumChannels
title: IDeviceModelPlugIn::GetNumChannels (wcsplugin.h)
description: Returns the number of device channels in the parameter pNumChannels.
helpviewer_keywords: ["GetNumChannels","GetNumChannels method [Windows Color System]","GetNumChannels method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","GetNumChannels method","IDeviceModelPlugIn.GetNumChannels","IDeviceModelPlugIn::GetNumChannels","_color_IDeviceModelPlugIn::GetNumChannels","wcs.IDeviceModelPlugIn_GetNumChannels","wcsplugin/IDeviceModelPlugIn::GetNumChannels"]
old-location: wcs\IDeviceModelPlugIn_GetNumChannels.htm
tech.root: WCS
ms.assetid: 3963eaf1-2516-4ac5-9f9f-9962f9d42adb
ms.date: 12/05/2018
ms.keywords: GetNumChannels, GetNumChannels method [Windows Color System], GetNumChannels method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetNumChannels method, IDeviceModelPlugIn.GetNumChannels, IDeviceModelPlugIn::GetNumChannels, _color_IDeviceModelPlugIn::GetNumChannels, wcs.IDeviceModelPlugIn_GetNumChannels, wcsplugin/IDeviceModelPlugIn::GetNumChannels
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
 - IDeviceModelPlugIn::GetNumChannels
 - wcsplugin/IDeviceModelPlugIn::GetNumChannels
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
 - IDeviceModelPlugIn.GetNumChannels
---

# IDeviceModelPlugIn::GetNumChannels


## -description

Returns the number of device channels in the parameter <i>pNumChannels</i>.

## -parameters

### -param pNumChannels [out]

A pointer to an unsigned integer representing the number of color channels for your device.

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)
