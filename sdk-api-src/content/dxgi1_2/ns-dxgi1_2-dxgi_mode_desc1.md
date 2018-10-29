---
UID: NS:dxgi1_2.DXGI_MODE_DESC1
title: DXGI_MODE_DESC1
author: windows-sdk-content
description: Describes a display mode and whether the display mode supports stereo.
old-location: direct3ddxgi\dxgi_mode_desc1.htm
tech.root: direct3ddxgi
ms.assetid: 8F44CF77-D3A1-44F7-AB7F-69E5727A4378
ms.author: windowssdkdev
ms.date: 10/26/2018
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

A <a href="https://msdn.microsoft.com/0a878d11-dc90-4cad-bde5-54a135e53a86">DXGI_RATIONAL</a> structure that describes the refresh rate in hertz.


### -field Format

A <a href="https://msdn.microsoft.com/dce61bc4-4ed5-4e64-84e8-6db88025e5c2">DXGI_FORMAT</a>-typed value that describes the display format.


### -field ScanlineOrdering

A <a href="https://msdn.microsoft.com/ecb66eed-9368-4cac-82e9-0e32c41e3ec5">DXGI_MODE_SCANLINE_ORDER</a>-typed value that describes the scan-line drawing mode.


### -field Scaling

A <a href="https://msdn.microsoft.com/2f9c16c6-b2d2-4135-8399-fd37aece3286">DXGI_MODE_SCALING</a>-typed value that describes the scaling mode.


### -field Stereo

Specifies whether the full-screen display mode is stereo. <b>TRUE</b> if stereo; otherwise, <b>FALSE</b>. 


## -remarks



<b>DXGI_MODE_DESC1</b> is identical to <a href="https://msdn.microsoft.com/ed39012c-0c3b-4c8e-ae83-c252c0fd3cff">DXGI_MODE_DESC</a> except that <b>DXGI_MODE_DESC1</b> includes the <b>Stereo</b> member.

This structure is used by the <a href="https://msdn.microsoft.com/49522ED9-30AD-4F39-96D2-BB6677D72349">GetDisplayModeList1</a> and <a href="https://msdn.microsoft.com/D71ED536-0D90-4E0D-8683-6260E31EAF20">FindClosestMatchingMode1</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/22e98880-bcd1-448a-9223-604fff9173fe">DXGI Structures</a>
 

 

