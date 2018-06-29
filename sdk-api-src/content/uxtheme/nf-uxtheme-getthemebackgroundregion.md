---
UID: NF:uxtheme.GetThemeBackgroundRegion
title: GetThemeBackgroundRegion function
author: windows-sdk-content
description: Computes the region for a regular or partially transparent background that is bounded by a specified rectangle.
old-location: controls\GetThemeBackgroundRegion.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemebackgroundregion.htm
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: GetThemeBackgroundRegion, GetThemeBackgroundRegion function [Windows Controls], controls.GetThemeBackgroundRegion, controls.inet_GetThemeBackgroundRegion, inet_GetThemeBackgroundRegion, inet_GetThemeBackgroundRegion_cpp, uxtheme/GetThemeBackgroundRegion
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: uxtheme.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: BP_BUFFERFORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
api_name:
 - GetThemeBackgroundRegion
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# GetThemeBackgroundRegion function


## -description


Computes the region for a regular or partially transparent background that is bounded by a specified rectangle.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to draw into. The DC uses dots per inch (DPI) scaling. This parameter may be set to <b>NULL</b>.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the region. See <a href="https://msdn.microsoft.com/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param pRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains, in logical coordinates, the specified rectangle used to compute the region. 


### -param pRegion [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRGN</a>*</b>

Pointer to the handle to the computed <a href="https://msdn.microsoft.com/library/windows/hardware/dn915769">region</a>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The region handle that is returned by this function should be released when it is no longer needed, using <a href="https://msdn.microsoft.com/cc679af0-6839-4c83-9c42-39d7ededda40">DeleteObject</a>. 




## -see-also




<b>Other Resources</b>



<a href="https://msdn.microsoft.com/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn915768">Regions</a>
 

 

