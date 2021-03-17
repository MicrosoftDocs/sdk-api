---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetNeutralAxisSize
title: IDeviceModelPlugIn::GetNeutralAxisSize (wcsplugin.h)
description: The IDeviceModelPlugIn::GetNeutralAxisSize function returns the number of data points along the neutral axis that are returned by the GetNeutralAxis function.
helpviewer_keywords: ["GetNeutralAxisSize","GetNeutralAxisSize method [Windows Color System]","GetNeutralAxisSize method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","GetNeutralAxisSize method","IDeviceModelPlugIn.GetNeutralAxisSize","IDeviceModelPlugIn::GetNeutralAxisSize","_color_IDeviceModelPlugIn::GetNeutralAxisSize","wcs.IDeviceModelPlugIn_GetNeutralAxisSize","wcsplugin/IDeviceModelPlugIn::GetNeutralAxisSize"]
old-location: wcs\IDeviceModelPlugIn_GetNeutralAxisSize.htm
tech.root: WCS
ms.assetid: a4b16003-b193-48b8-9dee-9ffb39f9159d
ms.date: 12/05/2018
ms.keywords: GetNeutralAxisSize, GetNeutralAxisSize method [Windows Color System], GetNeutralAxisSize method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetNeutralAxisSize method, IDeviceModelPlugIn.GetNeutralAxisSize, IDeviceModelPlugIn::GetNeutralAxisSize, _color_IDeviceModelPlugIn::GetNeutralAxisSize, wcs.IDeviceModelPlugIn_GetNeutralAxisSize, wcsplugin/IDeviceModelPlugIn::GetNeutralAxisSize
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
 - IDeviceModelPlugIn::GetNeutralAxisSize
 - wcsplugin/IDeviceModelPlugIn::GetNeutralAxisSize
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
 - IDeviceModelPlugIn.GetNeutralAxisSize
---

# IDeviceModelPlugIn::GetNeutralAxisSize


## -description

The <a href="/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxissize">IDeviceModelPlugIn::GetNeutralAxisSize</a> function returns the number of data points along the neutral axis that are returned by the <a href="/previous-versions/windows/desktop/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis">GetNeutralAxis</a> function. It is provided so that a Color Management Module (CMM) can allocate an appropriately sized buffer.

## -parameters

### -param pcColors [out]

The number of points that will be returned by a call to <a href="/previous-versions/windows/desktop/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis">GetNeutralAxis</a>. Minimum is 2 (black and white).

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)
