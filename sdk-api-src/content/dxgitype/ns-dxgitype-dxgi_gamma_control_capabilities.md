---
UID: NS:dxgitype.DXGI_GAMMA_CONTROL_CAPABILITIES
title: DXGI_GAMMA_CONTROL_CAPABILITIES
author: windows-sdk-content
description: Controls the gamma capabilities of an adapter.
old-location: direct3ddxgi\dxgi_gamma_control_capabilities.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_gamma_control_capabilities.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DXGI_GAMMA_CONTROL_CAPABILITIES, DXGI_GAMMA_CONTROL_CAPABILITIES structure [DXGI], direct3ddxgi.dxgi_gamma_control_capabilities, dxgitype/DXGI_GAMMA_CONTROL_CAPABILITIES, eb2a0d3b-fe87-b813-4911-af7ae107b1a1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgitype.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: DXGI_GAMMA_CONTROL_CAPABILITIES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgitype.h
api_name:
 - DXGI_GAMMA_CONTROL_CAPABILITIES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_GAMMA_CONTROL_CAPABILITIES structure


## -description


Controls the gamma capabilities of an adapter.


## -struct-fields




### -field ScaleAndOffsetSupported

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

True if scaling and offset operations are supported during gamma correction; otherwise, false.


### -field MaxConvertedValue

Type: <b>float</b>

A value describing the maximum range of the control-point positions.


### -field MinConvertedValue

Type: <b>float</b>

A value describing the minimum range of the control-point positions.


### -field NumGammaControlPoints

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A value describing the number of control points in the array.


### -field ControlPointPositions

Type: <b>float[1025]</b>

An array of values describing control points; the maximum length of control points is 1025.


## -remarks



To get a list of the capabilities for controlling gamma correction, call <a href="https://msdn.microsoft.com/bb9adbe7-74b2-41c6-987d-d292d0f80b62">IDXGIOutput::GetGammaControlCapabilities</a>.

For info about using gamma correction, see <a href="https://msdn.microsoft.com/97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A">Using gamma correction</a>. 




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

