---
UID: NF:wingdi.GetDCPenColor
title: GetDCPenColor function (wingdi.h)
author: windows-sdk-content
description: The GetDCPenColor function retrieves the current pen color for the specified device context (DC).
old-location: gdi\getdcpencolor.htm
tech.root: gdi
ms.assetid: 3a1d579f-fbc6-4021-a37e-0184b2cc7d5d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetDCPenColor, GetDCPenColor function [Windows GDI], _win32_GetDCPenColor, gdi.getdcpencolor, wingdi/GetDCPenColor
ms.topic: function
f1_keywords: ["wingdi/GetDCPenColor"]
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
 - Gdi32.dll
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32Full.dll
api_name:
 - GetDCPenColor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetDCPenColor function


## -description


The <b>GetDCPenColor</b> function retrieves the current pen color for the specified device context (DC).


## -parameters




### -param hdc [in]

A handle to the DC whose brush color is to be returned.


## -returns



If the function succeeds, the return value is a <a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a> value for the current DC pen color.

If the function fails, the return value is CLR_INVALID.




## -remarks



For information on setting the pen color, see <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setdcbrushcolor">SetDCPenColor</a>.

<b>ICM:</b> Color management is performed if ICM is enabled.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/colorref">COLORREF</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setdcpencolor">SetDCPenColor</a>
 

 

