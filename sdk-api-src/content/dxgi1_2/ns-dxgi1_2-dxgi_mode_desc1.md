---
UID: NS:dxgi1_2.DXGI_MODE_DESC1
title: DXGI_MODE_DESC1
author: windows-sdk-content
description: Describes a display mode and whether the display mode supports stereo.
old-location: direct3ddxgi\dxgi_mode_desc1.htm
tech.root: direct3ddxgi
ms.assetid: 8F44CF77-D3A1-44F7-AB7F-69E5727A4378
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: DXGI_MODE_DESC1, DXGI_MODE_DESC1 structure [DXGI], direct3ddxgi.dxgi_mode_desc1, dxgi1_2/DXGI_MODE_DESC1
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - HeaderDef
api_location:
 - DXGI1_2.h
api_name:
 - DXGI_MODE_DESC1
product: Windows
targetos: Windows
req.typenames: DXGI_MODE_DESC1
req.redist: 
---

# DXGI_MODE_DESC1 structure


## -description


Describes a display mode and whether the display mode supports stereo.


## -struct-fields




### -field Width

A value that describes the resolution width.


### -field Height

A value that describes the resolution height.


### -field RefreshRate

A <a href="https://msdn.microsoft.com/en-us/library/Bb173069(v=VS.85).aspx">DXGI_RATIONAL</a> structure that describes the refresh rate in hertz.


### -field Format

A <a href="https://msdn.microsoft.com/en-us/library/Bb173059(v=VS.85).aspx">DXGI_FORMAT</a>-typed value that describes the display format.


### -field ScanlineOrdering

A <a href="https://msdn.microsoft.com/en-us/library/Bb173067(v=VS.85).aspx">DXGI_MODE_SCANLINE_ORDER</a>-typed value that describes the scan-line drawing mode.


### -field Scaling

A <a href="https://msdn.microsoft.com/en-us/library/Bb173066(v=VS.85).aspx">DXGI_MODE_SCALING</a>-typed value that describes the scaling mode.


### -field Stereo

Specifies whether the full-screen display mode is stereo. <b>TRUE</b> if stereo; otherwise, <b>FALSE</b>. 


## -remarks



<b>DXGI_MODE_DESC1</b> is identical to <a href="https://msdn.microsoft.com/en-us/library/Bb173064(v=VS.85).aspx">DXGI_MODE_DESC</a> except that <b>DXGI_MODE_DESC1</b> includes the <b>Stereo</b> member.

This structure is used by the <a href="https://msdn.microsoft.com/49522ED9-30AD-4F39-96D2-BB6677D72349">GetDisplayModeList1</a> and <a href="https://msdn.microsoft.com/D71ED536-0D90-4E0D-8683-6260E31EAF20">FindClosestMatchingMode1</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

