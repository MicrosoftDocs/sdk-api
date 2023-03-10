---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetNeutralAxis
title: IDeviceModelPlugIn::GetNeutralAxis (wcsplugin.h)
description: The IDeviceModelPlugIn::GetNeutralAxis return the XYZ colorimetry of sample points along the device's neutral axis.
helpviewer_keywords: ["GetNeutralAxis","GetNeutralAxis method [Windows Color System]","GetNeutralAxis method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","GetNeutralAxis method","IDeviceModelPlugIn.GetNeutralAxis","IDeviceModelPlugIn::GetNeutralAxis","_color_IDeviceModelPlugIn::GetNeutralAxis","wcs.IDeviceModelPlugIn_GetNeutralAxis","wcsplugin/IDeviceModelPlugIn::GetNeutralAxis"]
old-location: wcs\IDeviceModelPlugIn_GetNeutralAxis.htm
tech.root: WCS
ms.assetid: 9a3557e0-d533-4357-aa2a-7e168482927a
ms.date: 12/05/2018
ms.keywords: GetNeutralAxis, GetNeutralAxis method [Windows Color System], GetNeutralAxis method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetNeutralAxis method, IDeviceModelPlugIn.GetNeutralAxis, IDeviceModelPlugIn::GetNeutralAxis, _color_IDeviceModelPlugIn::GetNeutralAxis, wcs.IDeviceModelPlugIn_GetNeutralAxis, wcsplugin/IDeviceModelPlugIn::GetNeutralAxis
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
 - IDeviceModelPlugIn::GetNeutralAxis
 - wcsplugin/IDeviceModelPlugIn::GetNeutralAxis
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
 - IDeviceModelPlugIn.GetNeutralAxis
---

# IDeviceModelPlugIn::GetNeutralAxis


## -description

The <a href="/windows/win32/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getneutralaxis">IDeviceModelPlugIn::GetNeutralAxis</a> return the XYZ colorimetry of sample points along the device's neutral axis.

## -parameters

### -param cColors [in]

The number of points that are returned.

### -param pXYZColors [out]

A pointer to an array of <a href="/windows/desktop/api/wcsplugin/ns-wcsplugin-xyzcolorf">XYZColorF</a> structures.

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.

## -remarks

You should define "neutral axis" in a way that is appropriate for your device. Usually, it is points made by the device's gray values. This might be R=G=B, or C=M=Y=0 and any value of K. For some devices, the most pleasing gray may be one that uses a different combination of colorants, such as M=Y=0 and C=K. The plug-in is responsible for determining the colorimetry of a sampling of the neutral axis values and returning them. The sampling may be as sparse as two points (white and black) or as dense as desired.

There is no requirement that the samples be uniformly spaced in any color space.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)
