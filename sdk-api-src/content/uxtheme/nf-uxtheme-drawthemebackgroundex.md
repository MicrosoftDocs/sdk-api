---
UID: NF:uxtheme.DrawThemeBackgroundEx
title: DrawThemeBackgroundEx function
author: windows-sdk-content
description: Draws the background image defined by the visual style for the specified control part.
old-location: controls\DrawThemeBackgroundEx.htm
tech.root: controls
ms.assetid: VS|Controls|~\controls\userex\functions\drawthemebackgroundex.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DrawThemeBackgroundEx, DrawThemeBackgroundEx function [Windows Controls], controls.DrawThemeBackgroundEx, controls.inet_DrawThemeBackgroundEx, inet_DrawThemeBackgroundEx, inet_DrawThemeBackgroundEx_cpp, uxtheme/DrawThemeBackgroundEx
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
req.lib: UxTheme.lib
req.dll: UxTheme.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - UxTheme.dll
 - ext-ms-win-uxtheme-themes-l1-1-1.dll
 - xamlpalwp.dll
api_name:
 - DrawThemeBackgroundEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DrawThemeBackgroundEx function


## -description


<p class="CCE_Message">[<b>DrawThemeBackgroundEx</b> is available for use in the operating 

systems specified in the Requirements section. It may be altered or unavailable in 

subsequent versions.]

Draws the background image defined by the visual style for the specified control part.


## -parameters




### -param hTheme [in]

Type: <b>HTHEME</b>

Handle to a window's specified theme data. Use <a href="https://msdn.microsoft.com/3c496a3f-e4d0-4938-af66-85df93829cd8">OpenThemeData</a> to create an HTHEME.


### -param hdc [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC used for drawing the theme-defined background image.


### -param iPartId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the part to draw. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param iStateId [in]

Type: <b>int</b>

Value of type <b>int</b> that specifies the state of the part to draw. See <a href="https://msdn.microsoft.com/97740fb8-c393-4c12-b5ef-9285220117f0">Parts and States</a>.


### -param pRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a> structure that contains the rectangle, in logical coordinates, in which the background image is drawn. 


### -param pOptions [in]

Type: <b>const <a href="https://msdn.microsoft.com/41793749-0685-48b6-be44-d3d1a7f4933f">DTBGOPTS</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/41793749-0685-48b6-be44-d3d1a7f4933f">DTBGOPTS</a> structure that contains clipping information. This parameter may be set to <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Drawing operations are scaled to fit and to not exceed the rectangle specified in <i>pRect</i>.



