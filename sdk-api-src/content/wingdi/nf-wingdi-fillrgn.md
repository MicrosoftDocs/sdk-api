---
UID: NF:wingdi.FillRgn
title: FillRgn function
author: windows-sdk-content
description: The FillRgn function fills a region by using the specified brush.
old-location: gdi\fillrgn.htm
tech.root: gdi
ms.assetid: c4e0eca5-442b-462b-a4f2-0c628b6d3d38
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: FillRgn, FillRgn function [Windows GDI], _win32_FillRgn, gdi.fillrgn, wingdi/FillRgn
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wingdi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdi32.lib
req.dll: Gdi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - gdi32.dll
 - Ext-MS-Win-GDI-rgn-l1-1-0.dll
 - Ext-MS-Win-RTCore-GDI-rgn-l1-1-0.dll
 - ext-ms-win-rtcore-gdi-rgn-l1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
 - GDI32Min.dll
api_name:
 - FillRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FillRgn function


## -description


The <b>FillRgn</b> function fills a region by using the specified brush.


## -parameters




### -param hdc [in]

Handle to the device context.


### -param hrgn [in]

Handle to the region to be filled. The region's coordinates are presumed to be in logical units.


### -param hbr [in]

Handle to the brush to be used to fill the region.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero.




## -see-also




<a href="https://msdn.microsoft.com/75f94ad1-ca25-4ad1-9e8c-ad1a4b8475a7">CreateBrushIndirect</a>



<a href="https://msdn.microsoft.com/d123ef44-e047-4188-a2bc-20e479869dc3">CreateDIBPatternBrush</a>



<a href="https://msdn.microsoft.com/0b5849d6-1e22-4ac5-980c-2f2a73b16adb">CreateHatchBrush</a>



<a href="https://msdn.microsoft.com/a3cf347e-9803-4bb0-bdb3-98929ef859ab">CreatePatternBrush</a>



<a href="https://msdn.microsoft.com/e39b5f77-97d8-4ea6-8277-7da12b3367f3">CreateSolidBrush</a>



<a href="https://msdn.microsoft.com/7656fb67-d865-459e-b379-4f2e44c76fd0">PaintRgn</a>



<a href="https://msdn.microsoft.com/3a42fc7a-4c07-4540-99a7-520f99532f33">Region Functions</a>



<a href="https://msdn.microsoft.com/5d2e8624-4d1a-44f7-821e-a54f6f538214">Regions Overview</a>
 

 

