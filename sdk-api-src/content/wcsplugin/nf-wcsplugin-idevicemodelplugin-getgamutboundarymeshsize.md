---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetGamutBoundaryMeshSize
title: IDeviceModelPlugIn::GetGamutBoundaryMeshSize (wcsplugin.h)
description: Returns the required data structure sizes for the GetGamutBoundaryMesh function.
helpviewer_keywords: ["GetGamutBoundaryMeshSize","GetGamutBoundaryMeshSize method [Windows Color System]","GetGamutBoundaryMeshSize method [Windows Color System]","IDeviceModelPlugIn interface","IDeviceModelPlugIn interface [Windows Color System]","GetGamutBoundaryMeshSize method","IDeviceModelPlugIn.GetGamutBoundaryMeshSize","IDeviceModelPlugIn::GetGamutBoundaryMeshSize","_color_IDeviceModelPlugIn::GetGamutBoundaryMeshSize","wcs.IDeviceModelPlugIn_GetGamutBoundaryMeshSize","wcsplugin/IDeviceModelPlugIn::GetGamutBoundaryMeshSize"]
old-location: wcs\IDeviceModelPlugIn_GetGamutBoundaryMeshSize.htm
tech.root: WCS
ms.assetid: 302f8008-c65d-4794-9297-8b47e29e36ce
ms.date: 12/05/2018
ms.keywords: GetGamutBoundaryMeshSize, GetGamutBoundaryMeshSize method [Windows Color System], GetGamutBoundaryMeshSize method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetGamutBoundaryMeshSize method, IDeviceModelPlugIn.GetGamutBoundaryMeshSize, IDeviceModelPlugIn::GetGamutBoundaryMeshSize, _color_IDeviceModelPlugIn::GetGamutBoundaryMeshSize, wcs.IDeviceModelPlugIn_GetGamutBoundaryMeshSize, wcsplugin/IDeviceModelPlugIn::GetGamutBoundaryMeshSize
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
 - IDeviceModelPlugIn::GetGamutBoundaryMeshSize
 - wcsplugin/IDeviceModelPlugIn::GetGamutBoundaryMeshSize
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
 - IDeviceModelPlugIn.GetGamutBoundaryMeshSize
---

# IDeviceModelPlugIn::GetGamutBoundaryMeshSize


## -description

Returns the required data structure sizes for the <a href="/previous-versions/windows/desktop/api/wcsplugin/nf-wcsplugin-idevicemodelplugin-getgamutboundarymesh">GetGamutBoundaryMesh</a> function.

## -parameters

### -param pNumVertices [out]

The required number of vertices.

### -param pNumTriangles [out]

The required number of triangles.

## -returns

If this function succeeds, the return value is S_OK.

If the plug-in device model wants WCS to compute its gamut boundary mesh, the return value is S_FALSE.

If this function fails, the return value is E_FAIL.

## -remarks

This function is called by the [CreateMultiProfileTransform](/windows/win32/api/icm/nf-icm-createmultiprofiletransform) function.

## -see-also

* [Basic color management concepts](/windows/win32/wcs/basic-color-management-concepts)
* [Functions](/windows/win32/wcs/functions)
* [IDeviceModelPlugIn](/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin)
