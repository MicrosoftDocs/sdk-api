---
UID: NF:uxtheme.GetThemeBackgroundExtent
title: GetThemeBackgroundExtent function
author: windows-driver-content
description: Calculates the size and location of the background, defined by the visual style, given the content area.
old-location: controls\GetThemeBackgroundExtent.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemebackgroundextent.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetThemeBackgroundExtent, GetThemeBackgroundExtent function [Windows Controls], controls.GetThemeBackgroundExtent, controls.inet_GetThemeBackgroundExtent, inet_GetThemeBackgroundExtent, inet_GetThemeBackgroundExtent_cpp, uxtheme/GetThemeBackgroundExtent
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
-	Ext-MS-Win-UXTheme-Themes-l1-1-0.dll
-	xamlpalwp.dll
-	ext-ms-win-uxtheme-themes-l1-1-1.dll
api_name:
-	GetThemeBackgroundExtent
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# GetThemeBackgroundExtent function


## -description


Calculates the size and location of the background, defined by the visual style, given the content area.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to use when drawing. This parameter may be set to <b>NULL</b>.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part that contains the content. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part that contains the content. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param pContentRect [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the content background rectangle, in logical coordinates. This rectangle is returned from <a href="https://msdn.microsoft.com/84520924-3f41-47b0-b8b1-442430cc113e">GetThemeBackgroundContentRect</a>.


### -param pExtentRect [out]

Type: <b>LPRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that receives the background rectangle, in logical coordinates. This rectangle is based on the <i>pContentRect</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A theme can define a content area within each background image. This is the area where content such as text and icons can be placed without overwriting background borders.




## -see-also




<a href="https://msdn.microsoft.com/84520924-3f41-47b0-b8b1-442430cc113e">GetThemeBackgroundContentRect</a>



<a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>



<b>Reference</b>
 

 

