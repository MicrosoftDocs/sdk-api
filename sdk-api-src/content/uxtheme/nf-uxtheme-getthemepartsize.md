---
UID: NF:uxtheme.GetThemePartSize
title: GetThemePartSize function
author: windows-driver-content
description: Calculates the original size of the part defined by a visual style.
old-location: controls\GetThemePartSize.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\userex\functions\getthemepartsize.htm
ms.author: windowsdriverdev
ms.date: 5/17/2018
ms.keywords: GetThemePartSize, GetThemePartSize function [Windows Controls], controls.GetThemePartSize, controls.inet_GetThemePartSize, inet_GetThemePartSize, inet_GetThemePartSize_cpp, uxtheme/GetThemePartSize
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
-	GetThemePartSize
product: Windows
targetos: Windows
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
req.product: Windows UI
---

# GetThemePartSize function


## -description


Calculates the original size of the part defined by a visual style.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC to select fonts into.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part to calculate the size of. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param prc [in]

Type: <b>LPCRECT</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains the rectangle used for the part drawing destination. This parameter may be set to <b>NULL</b>.


### -param eSize [in]

Type: <b>THEMESIZE</b>

Enumerated type that specifies the type of size to retrieve. See <a href="https://msdn.microsoft.com/099d3d2d-a267-429c-abf5-6632bc8bc92a">THEMESIZE</a> for a list of type values.


### -param psz [out]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure that receives the dimensions of the specified part.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b0e22022-fea9-43d1-8ef0-7a1c518760f1">Property Identifiers</a>
 

 

