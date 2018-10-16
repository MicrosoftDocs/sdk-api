---
UID: NF:wingdi.GetRandomRgn
title: GetRandomRgn function
author: windows-sdk-content
description: The GetRandomRgn function copies the system clipping region of a specified device context to a specific region.
old-location: gdi\getrandomrgn.htm
tech.root: gdi
ms.assetid: a7527d7a-7b5e-4dd5-9270-94bc92b5a4a0
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: GetRandomRgn, GetRandomRgn function [Windows GDI], _win32_GetRandomRgn, gdi.getrandomrgn, wingdi/GetRandomRgn
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
 - Ext-MS-Win-RTCore-GDI-Rgn-L1-1-1.dll
 - API-MS-Win-GDI-Internal-Uap-L1-1-0.dll
 - GDI32Full.dll
 - GDI32Min.dll
api_name:
 - GetRandomRgn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetRandomRgn function


## -description


The <b>GetRandomRgn</b> function copies the system clipping region of a specified device context to a specific region.


## -parameters




### -param hdc [in]

A handle to the device context.


### -param hrgn [in]

A handle to a region. Before the function is called, this identifies an existing region. After the function returns, this identifies a copy of the current system region. The old region identified by <i>hrgn</i> is overwritten.


### -param i [in]

This parameter must be SYSRGN.


## -returns



If the function succeeds, the return value is 1. If the function fails, the return value is -1. If the region to be retrieved is <b>NULL</b>, the return value is 0. If the function fails or the region to be retrieved is <b>NULL</b>, <i>hrgn</i> is not initialized.




## -remarks



When using the SYSRGN flag, note that the system clipping region might not be current because of window movements. Nonetheless, it is safe to retrieve and use the system clipping region within the <a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>-<a href="https://msdn.microsoft.com/b07cfed9-21c4-4459-855a-eaf4d1d34ab8">EndPaint</a> block during <a href="https://msdn.microsoft.com/afebaa07-cf00-47db-a919-46436f164881">WM_PAINT</a> processing. In this case, the system region is the intersection of the update region and the current visible area of the window. Any window movement following the return of <b>GetRandomRgn</b> and before <b>EndPaint</b> will result in a new <b>WM_PAINT</b> message. Any other use of the SYSRGN flag may result in painting errors in your application.

The region returned is in screen coordinates.




## -see-also




<a href="https://msdn.microsoft.com/513341d7-bed8-469c-a067-ee71dc8860f9">BeginPaint</a>



<a href="https://msdn.microsoft.com/de9e5786-63d8-47be-8522-e96d7c0f8634">Clipping Functions</a>



<a href="https://msdn.microsoft.com/9e966369-9988-4bfa-af37-b1bbb3488880">Clipping Overview</a>



<a href="https://msdn.microsoft.com/b07cfed9-21c4-4459-855a-eaf4d1d34ab8">EndPaint</a>



<a href="https://msdn.microsoft.com/d222defe-2ef9-4622-b2e1-462a91cb1b0a">ExtSelectClipRgn</a>



<a href="https://msdn.microsoft.com/b4ee68ab-b99e-48b6-90ce-6d6c0ae144e2">GetClipBox</a>



<a href="https://msdn.microsoft.com/66c807b8-129f-40f2-b8d8-995e0a5e22e4">GetClipRgn</a>



<a href="https://msdn.microsoft.com/e0d4862d-a405-4c00-b7b0-af4dd60407c0">GetRegionData</a>



<a href="https://msdn.microsoft.com/5228c614-3278-4852-a867-7eed57359aef">OffsetRgn</a>
 

 

