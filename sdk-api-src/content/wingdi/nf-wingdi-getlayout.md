---
UID: NF:wingdi.GetLayout
title: GetLayout function (wingdi.h)
description: The GetLayout function returns the layout of a device context (DC).
helpviewer_keywords: ["GetLayout","GetLayout function [Windows GDI]","_win32_GetLayout","gdi.getlayout","wingdi/GetLayout"]
old-location: gdi\getlayout.htm
tech.root: gdi
ms.assetid: 2bbc0bef-55e5-4f11-a195-d379e95e44bf
ms.date: 12/05/2018
ms.keywords: GetLayout, GetLayout function [Windows GDI], _win32_GetLayout, gdi.getlayout, wingdi/GetLayout
f1_keywords:
- wingdi/GetLayout
dev_langs:
- c++
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
- ext-ms-win-gdi-dc-l1-2-1.dll
- GDI32Full.dll
api_name:
- GetLayout
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetLayout function


## -description


The <b>GetLayout</b> function returns the layout of a device context (DC).


## -parameters




### -param hdc [in]

A handle to the device context.


## -returns



If the function succeeds, it returns the layout flags for the current device context.

If the function fails, it returns GDI_ERROR. For extended error information, call <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



The layout specifies the order in which text and graphics are revealed in a window or device context. The default is left to right. The <b>GetLayout</b> function tells you if the default has been changed through a call to <a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setlayout">SetLayout</a>. For more information, see "Window Layout and Mirroring" in <a href="https://docs.microsoft.com/windows/desktop/winmsg/window-features">Window Features</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/gdi/device-context-functions">Device Context Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/gdi/device-contexts">Device Contexts Overview</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wingdi/nf-wingdi-setlayout">SetLayout</a>
 

 

