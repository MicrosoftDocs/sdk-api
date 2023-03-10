---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetGamutBoundaryMesh
title: IDeviceModelPlugIn::GetGamutBoundaryMesh (wcsplugin.h)
description: Returns the triangular mesh from the plug-in. This function is used to compute the GamutBoundaryDescription.
helpviewer_keywords: ["GetGamutBoundaryMesh","GetGamutBoundaryMesh method [Windows Color System]","GetGamutBoundaryMesh method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","GetGamutBoundaryMesh method","IDeviceModelPlugIn.GetGamutBoundaryMesh","IDeviceModelPlugIn::GetGamutBoundaryMesh","_color_IDeviceModelPlugIn::GetGamutBoundaryMesh","wcs.IDeviceModelPlugIn_GetGamutBoundaryMesh","wcsplugin/IDeviceModelPlugIn::GetGamutBoundaryMesh"]
old-location: wcs\IDeviceModelPlugIn_GetGamutBoundaryMesh.htm
tech.root: WCS
ms.assetid: 275269d3-e542-41b3-80d6-e1c90f296456
ms.date: 12/05/2018
ms.keywords: GetGamutBoundaryMesh, GetGamutBoundaryMesh method [Windows Color System], GetGamutBoundaryMesh method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetGamutBoundaryMesh method, IDeviceModelPlugIn.GetGamutBoundaryMesh, IDeviceModelPlugIn::GetGamutBoundaryMesh, _color_IDeviceModelPlugIn::GetGamutBoundaryMesh, wcs.IDeviceModelPlugIn_GetGamutBoundaryMesh, wcsplugin/IDeviceModelPlugIn::GetGamutBoundaryMesh
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
 - IDeviceModelPlugIn::GetGamutBoundaryMesh
 - wcsplugin/IDeviceModelPlugIn::GetGamutBoundaryMesh
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
 - IDeviceModelPlugIn.GetGamutBoundaryMesh
---

# IDeviceModelPlugIn::GetGamutBoundaryMesh


## -description

Returns the triangular mesh from the plug-in. This function is used to compute the GamutBoundaryDescription.

## -parameters

### -param cChannels [in]

The number of channels.

### -param cVertices [in]

The number of vertices.

### -param cTriangles [in]

The number of triangles.

### -param pVertices [out]

A pointer to the array of vertices in the plug-in model gamut shell.

### -param pTriangles [out]

A pointer to the array of triangles in the plug-in model gamut shell.

## -returns

If this function succeeds, the return value is S_OK.

If this function fails, the return value is E_FAIL.

## -remarks

This function is called by the [CreateMultiProfileTransform](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) function.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)
