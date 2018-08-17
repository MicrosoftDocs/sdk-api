---
UID: NF:wcsplugin.IDeviceModelPlugIn.GetGamutBoundaryMesh
title: IDeviceModelPlugIn::GetGamutBoundaryMesh
author: windows-sdk-content
description: Returns the triangular mesh from the plug-in. This function is used to compute the GamutBoundaryDescription.
old-location: wcs\IDeviceModelPlugIn_GetGamutBoundaryMesh.htm
old-project: WCS
ms.assetid: 275269d3-e542-41b3-80d6-e1c90f296456
ms.author: windowssdkdev
ms.date: 08/15/2018
ms.keywords: GetGamutBoundaryMesh, GetGamutBoundaryMesh method [Windows Color System], GetGamutBoundaryMesh method [Windows Color System],IDeviceModelPlugIn interface, IDeviceModelPlugIn interface [Windows Color System],GetGamutBoundaryMesh method, IDeviceModelPlugIn.GetGamutBoundaryMesh, IDeviceModelPlugIn::GetGamutBoundaryMesh, _color_IDeviceModelPlugIn::GetGamutBoundaryMesh, wcs.IDeviceModelPlugIn_GetGamutBoundaryMesh, wcsplugin/IDeviceModelPlugIn::GetGamutBoundaryMesh
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wcsplugin.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WCN_VALUE_TYPE_PRIMARY_DEVICE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WcsPlugIn.h
api_name:
 - IDeviceModelPlugIn.GetGamutBoundaryMesh
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
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



This function is called by the <a href="https://msdn.microsoft.com/8a40215c-6c37-4346-a669-79b7871f265e">CreateMultiProfileTransform</a> function.




## -see-also




<a href="https://msdn.microsoft.com/a0623917-0b63-4546-a71a-1e9efa9fe8e5">Basic Color Management Concepts</a>



<a href="https://msdn.microsoft.com/ee9e9502-5514-4070-95fa-265674a1dde7">Functions</a>



<a href="https://msdn.microsoft.com/90541ec2-c0ab-4f98-906b-3e58f8f5cc03">IDeviceModelPlugIn</a>
 

 

