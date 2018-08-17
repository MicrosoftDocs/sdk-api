---
UID: NS:dxgitype.DXGI_GAMMA_CONTROL
title: DXGI_GAMMA_CONTROL
author: windows-sdk-content
description: Controls the settings of a gamma curve.
old-location: direct3ddxgi\dxgi_gamma_control.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\dxgi_gamma_control.htm
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: DXGI_GAMMA_CONTROL, DXGI_GAMMA_CONTROL structure [DXGI], direct3ddxgi.dxgi_gamma_control, dxgitype/DXGI_GAMMA_CONTROL, ebef8c66-066b-5a1e-82b2-7543213beff2
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
req.typenames: DXGI_GAMMA_CONTROL
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dxgitype.h
api_name:
 - DXGI_GAMMA_CONTROL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# DXGI_GAMMA_CONTROL structure


## -description


Controls the settings of a gamma curve.


## -struct-fields




### -field Scale

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173071(v=VS.85).aspx">DXGI_RGB</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb173071(v=VS.85).aspx">DXGI_RGB</a> structure with scalar values that are applied to rgb values before being sent to the gamma look up table.


### -field Offset

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173071(v=VS.85).aspx">DXGI_RGB</a></b>

A <a href="https://msdn.microsoft.com/en-us/library/Bb173071(v=VS.85).aspx">DXGI_RGB</a> structure with offset values that are applied to the rgb values before being sent to the gamma look up table.


### -field GammaCurve

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb173071(v=VS.85).aspx">DXGI_RGB</a>[1025]</b>

An array of <a href="https://msdn.microsoft.com/en-us/library/Bb173071(v=VS.85).aspx">DXGI_RGB</a> structures that control the points of a gamma curve.


## -remarks



The <b>DXGI_GAMMA_CONTROL</b> structure is used by the <a href="https://msdn.microsoft.com/en-us/library/Bb174557(v=VS.85).aspx">IDXGIOutput::SetGammaControl</a> method.

For info about using gamma correction, see <a href="https://msdn.microsoft.com/97ACDAE3-514E-4AAF-A27D-E5FFC162DB2A">Using gamma correction</a>. 




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

