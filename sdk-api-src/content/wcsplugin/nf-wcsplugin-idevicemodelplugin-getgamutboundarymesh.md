---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetGamutBoundaryMesh
title: IDeviceModelPlugIn::GetGamutBoundaryMesh (wcsplugin.h)
author: windows-sdk-content
description: Returns the triangular mesh from the plug-in. This function is used to compute the GamutBoundaryDescription.
old-location: wcs\IDeviceModelPlugIn_GetGamutBoundaryMesh.htm
tech.root: WCS
ms.assetid: 275269d3-e542-41b3-80d6-e1c90f296456
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetGamutBoundaryMesh, GetGamutBoundaryMesh method [Windows Color System], GetGamutBoundaryMesh method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetGamutBoundaryMesh method, IDeviceModelPlugIn.GetGamutBoundaryMesh, IDeviceModelPlugIn::GetGamutBoundaryMesh, _color_IDeviceModelPlugIn::GetGamutBoundaryMesh, wcs.IDeviceModelPlugIn_GetGamutBoundaryMesh, wcsplugin/IDeviceModelPlugIn::GetGamutBoundaryMesh
ms.topic: method
f1_keywords: 
 - "wcsplugin/IDeviceModelPlugIn.GetGamutBoundaryMesh"
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
 - IDeviceModelPlugIn.GetGamutBoundaryMesh
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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



This function is called by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/createmultiprofiletransform">CreateMultiProfileTransform</a> function.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/wcs/basic-color-management-concepts">Basic Color Management Concepts</a>



<a href="https://docs.microsoft.com/previous-versions/dd316902(v=vs.85)">Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/wcsplugin/nn-wcsplugin-idevicemodelplugin">IDeviceModelPlugIn</a>
 

 

