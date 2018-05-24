---
UID: NF:commctrl.DrawShadowText
title: DrawShadowText function
author: windows-driver-content
description: Draws text that has a shadow.
old-location: controls\DrawShadowText.htm
old-project: Controls
ms.assetid: VS|Controls|~\controls\common\functions\drawshadowtext.htm
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: DrawShadowText, DrawShadowText function [Windows Controls], commctrl/DrawShadowText, controls.DrawShadowText, controls.inet_DrawShadowText, inet_DrawShadowText, inet_DrawShadowText_cpp
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: commctrl.h
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
req.typenames: STGOPTIONS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ComCtl32.dll
api_name:
-	DrawShadowText
product: Windows
targetos: Windows
req.lib: Comctl32.lib
req.dll: ComCtl32.dll (version 6 or later)
req.irql: 
---

# DrawShadowText function


## -description


Draws text that has a shadow.


## -parameters




### -param hdc

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

HDC.


### -param pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCWSTR</a></b>

A pointer to a string that contains the text to be drawn.


### -param cch

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A <b>UINT</b> that specifies the number of characters in the string that is to be drawn.


### -param prc

TBD


### -param dwFlags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

A <b>DWORD</b> that specifies how the text is to be drawn. See <a href="https://msdn.microsoft.com/765b90df-4753-43e6-bcf7-6512f6f378bd">Format Values</a> for possible parameter values. 


### -param crText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure that contains the color of the text.


### -param crShadow

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">COLORREF</a></b>

A <a href="https://msdn.microsoft.com/b87d3de2-7a13-44ef-8253-c6851a75fa54">COLORREF</a> structure that contains the color of the text shadow.


### -param ixOffset

Type: <b>int</b>

A value of type <b>int</b> that specifies the x-coordinate of where the text should begin.


### -param iyOffset

Type: <b>int</b>

A value of type <b>int</b> that specifies the y-coordinate of where the text should begin.


#### - pRect

Type: <b>const <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff569234">RECT</a> structure that contains, in logical coordinates, the rectangle in which the text is to be drawn.


## -returns



Type: <b>int</b>

Returns the height of the text in logical units if the function succeeds, otherwise returns zero.




## -remarks



To use <b>DrawShadowText</b>, specify Comctl32.dll version 6 in the manifest. For more information on manifests, see <a href="https://msdn.microsoft.com/eb6c2469-25b9-43c4-a6ca-391a7b2859b3">Enabling Visual Styles</a>. 



