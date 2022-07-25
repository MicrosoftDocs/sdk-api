---
UID: NF:gdiplusbrush.Brush.GetLastStatus
title: Brush::GetLastStatus (gdiplusbrush.h)
description: The Brush::GetLastStatus method returns a value that indicates the nature of this Brush object's most recent method failure.
helpviewer_keywords: ["Brush class [GDI+]","GetLastStatus method","Brush.GetLastStatus","Brush::GetLastStatus","GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","Brush class","_gdiplus_CLASS_Brush_GetLastStatus_","gdiplus._gdiplus_CLASS_Brush_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_Brush_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\brushclass\brushmethods\getlaststatus.htm
ms.date: 12/05/2018
ms.keywords: Brush class [GDI+],GetLastStatus method, Brush.GetLastStatus, Brush::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],Brush class, _gdiplus_CLASS_Brush_GetLastStatus_, gdiplus._gdiplus_CLASS_Brush_GetLastStatus_
req.header: gdiplusbrush.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Brush::GetLastStatus
 - gdiplusbrush/Brush::GetLastStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Brush.GetLastStatus
---

# Brush::GetLastStatus


## -description

The <b>Brush::GetLastStatus</b> method returns a value that indicates the nature of this 
			<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object's most recent method failure.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The <b>Brush::GetLastStatus</b> method returns an element of the 	<a href="/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If no methods invoked on this 
						<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object have failed since the previous call to <b>Brush::GetLastStatus</b>, then <b>Brush::GetLastStatus</b> returns Ok.

If at least one method invoked on this 
						<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object has failed since the previous call to <b>Brush::GetLastStatus</b>, then <b>Brush::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.

## -remarks

You can call <b>Brush::GetLastStatus</b> immediately after constructing a 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object to determine whether the constructor succeeded.

The first time you call the <b>Brush::GetLastStatus</b> method of a 
				<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a> object, it returns Ok if the constructor succeeded and all methods invoked so far on the 
				<b>Brush</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.


#### Examples



The following example creates a <a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a> object 
						<b>solidBrush</b> and checks the status of the call used to create 
						<b>solidBrush</b>. Then, if the call was successful, the code uses 
						<b>solidBrush</b> to fill a rectangle.


```cpp
VOID Example_GetLastStatus(HDC hdc)
{
   Graphics graphics(hdc);
   // Create a SolidBrush object.
   SolidBrush solidBrush(Color(255, 0, 255, 0));
   // Get the status of the last call.
   Status lastStatus = solidBrush.GetLastStatus();
   //If the call to create myBrush was successful, use it to fill a rectangle.
   if (lastStatus == Ok)
       graphics.FillRectangle(&solidBrush, Rect(0, 0, 100, 100)); 
}
```

## -see-also

<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-brush">Brush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-brushes-and-filled-shapes-about">Brushes and Filled Shapes</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-hatchbrush">HatchBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-lineargradientbrush">LinearGradientBrush</a>



<a href="/windows/desktop/api/gdipluspath/nl-gdipluspath-pathgradientbrush">PathGradientBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-solidbrush">SolidBrush</a>



<a href="/windows/desktop/api/gdiplusbrush/nl-gdiplusbrush-texturebrush">TextureBrush</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-a-brush-to-fill-shapes-use">Using a Brush to Fill Shapes</a>
