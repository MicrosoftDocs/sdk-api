---
UID: NF:winuser.GetDC
title: GetDC function
author: windows-sdk-content
description: The GetDC function retrieves a handle to a device context (DC) for the client area of a specified window or for the entire screen.
old-location: gdi\getdc.htm
tech.root: gdi
ms.assetid: 50b2387b-c8e4-42a8-8f0f-0bdb355adbfd
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: GetDC, GetDC function [Windows GDI], _win32_GetDC, gdi.getdc, winuser/GetDC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winuser.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - user32.dll
 - Ext-MS-Win-NTUser-DC-Access-Ext-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-DC-Access-l1-1-0.dll
 - minuser.dll
 - api-ms-win-ntuser-dc-access-l1-1-0.dll
 - Ext-MS-Win-RTCore-NTUser-DC-Access-L1-1-1.dll
api_name:
 - GetDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# GetDC function


## -description


The <b>GetDC</b> function retrieves a handle to a device context (DC) for the client area of a specified window or for the entire screen. You can use the returned handle in subsequent GDI functions to draw in the DC. The device context is an opaque data structure, whose values are used internally by GDI.

The <a href="https://msdn.microsoft.com/590cf928-0ad6-43f8-97e9-1dafbcfa9f49">GetDCEx</a> function is an extension to <b>GetDC</b>, which gives an application more control over how and whether clipping occurs in the client area.


## -parameters




### -param hWnd [in]

A handle to the window whose DC is to be retrieved. If this value is <b>NULL</b>, <b>GetDC</b> retrieves the DC for the entire screen.


## -returns



If the function succeeds, the return value is a handle to the DC for the specified window's client area.

If the function fails, the return value is <b>NULL</b>.




## -remarks



The <b>GetDC</b> function retrieves a common, class, or private DC depending on the class style of the specified window. For class and private DCs, <b>GetDC</b> leaves the previously assigned attributes unchanged. However, for common DCs, <b>GetDC</b> assigns default attributes to the DC each time it is retrieved. For example, the default font is System, which is a bitmap font. Because of this, the handle to a common DC returned by <b>GetDC</b> does not tell you what font, color, or brush was used when the window was drawn. To determine the font, call <a href="https://msdn.microsoft.com/c4c8c8f5-3651-481b-a55f-da7f49d92f3a">GetTextFace</a>.

Note that the handle to the DC can only be used by a single thread at any one time.

After painting with a common DC, the <a href="https://msdn.microsoft.com/c4f48f1e-4a37-4330-908e-2ac5c65e1a1d">ReleaseDC</a> function must be called to release the DC. Class and private DCs do not have to be released. <b>ReleaseDC</b> must be called from the same thread that called <b>GetDC</b>. The number of DCs is limited only by available memory. 


#### Examples

For an example, see <a href="https://msdn.microsoft.com/5e8a54b6-05cc-4446-b82e-2b3e550d780a">Drawing with the Mouse</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9ff68d16-0f27-4cc8-932a-b2063cfed135">Device Context Functions</a>



<a href="https://msdn.microsoft.com/1fa97368-8931-4687-b37f-ed4db949a150">Device Contexts Overview</a>



<a href="https://msdn.microsoft.com/590cf928-0ad6-43f8-97e9-1dafbcfa9f49">GetDCEx</a>



<a href="https://msdn.microsoft.com/c4c8c8f5-3651-481b-a55f-da7f49d92f3a">GetTextFace</a>



<a href="https://msdn.microsoft.com/9e6a135e-e337-4129-a3ad-faf9a8ac9b2d">GetWindowDC</a>



<a href="https://msdn.microsoft.com/c4f48f1e-4a37-4330-908e-2ac5c65e1a1d">ReleaseDC</a>



<a href="https://msdn.microsoft.com/57ecec82-03be-4d1a-84cf-6b64131af19d">WindowFromDC</a>
 

 

