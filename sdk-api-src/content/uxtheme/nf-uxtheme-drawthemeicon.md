---
UID: NF:uxtheme.DrawThemeIcon
title: DrawThemeIcon function
author: windows-driver-content
description: Draws an image from an image list with the icon effect defined by the visual style.
old-location: controls\DrawThemeIcon.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemeicon.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DrawThemeIcon, DrawThemeIcon function [Windows Controls], controls.DrawThemeIcon, controls.inet_DrawThemeIcon, inet_DrawThemeIcon, inet_DrawThemeIcon_cpp, uxtheme/DrawThemeIcon
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: BP_BUFFERFORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	UxTheme.dll
api_name:
-	DrawThemeIcon
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

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part in which the image is drawn. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param pRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains, in logical coordinates, the rectangle in which the image is drawn.


### -param himl [in]

Type: <b>HIMAGELIST</b>

Handle to an <a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">image list</a> that contains the image to draw.


### -param iImageIndex [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the index of the image to draw.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/02e397a4-22fa-49fb-8103-376aa5ebc77a">IImageList</a>



<a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>



<b>Reference</b>
 

 

