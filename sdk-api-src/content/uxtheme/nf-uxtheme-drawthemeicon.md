---
UID: NF:uxtheme.DrawThemeIcon
title: DrawThemeIcon function
author: windows-sdk-content
description: Draws an image from an image list with the icon effect defined by the visual style.
old-location: controls\DrawThemeIcon.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemeicon.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrawThemeIcon, DrawThemeIcon function [Windows Controls], controls.DrawThemeIcon, controls.inet_DrawThemeIcon, inet_DrawThemeIcon, inet_DrawThemeIcon_cpp, uxtheme/DrawThemeIcon
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
 - DrawThemeIcon
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# DrawThemeIcon function


## -description


Draws an image from an image list with the icon effect defined by the visual style.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/en-us/library/Bb759821(v=VS.85).aspx">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part in which the image is drawn. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/en-us/library/Bb773210(v=VS.85).aspx">Parts and States</a>.


### -param pRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains, in logical coordinates, the rectangle in which the image is drawn.


### -param himl [in]

Type: <b>HIMAGELIST</b>

Handle to an <a href="https://msdn.microsoft.com/en-us/library/Bb761490(v=VS.85).aspx">image list</a> that contains the image to draw.


### -param iImageIndex [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the index of the image to draw.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761490(v=VS.85).aspx">IImageList</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773213(v=VS.85).aspx">Property Identifiers</a>



<b>Reference</b>
 

 

