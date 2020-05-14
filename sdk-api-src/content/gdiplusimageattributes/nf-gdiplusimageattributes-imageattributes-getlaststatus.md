---
UID: NF:gdiplusimageattributes.ImageAttributes.GetLastStatus
title: ImageAttributes::GetLastStatus (gdiplusimageattributes.h)
description: The ImageAttributes::GetLastStatus method returns a value that indicates the nature of this ImageAttributes object's most recent method failure.helpviewer_keywords: ["GetLastStatus","GetLastStatus method [GDI+]","GetLastStatus method [GDI+]","ImageAttributes class","ImageAttributes class [GDI+]","GetLastStatus method","ImageAttributes.GetLastStatus","ImageAttributes::GetLastStatus","_gdiplus_CLASS_ImageAttributes_GetLastStatus_","gdiplus._gdiplus_CLASS_ImageAttributes_GetLastStatus_"]
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\getlaststatus_2.htm
ms.date: 12/05/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],GetLastStatus method, ImageAttributes.GetLastStatus, ImageAttributes::GetLastStatus, _gdiplus_CLASS_ImageAttributes_GetLastStatus_, gdiplus._gdiplus_CLASS_ImageAttributes_GetLastStatus_
f1_keywords:
- gdiplusimageattributes/ImageAttributes.GetLastStatus
dev_langs:
- c++
req.header: gdiplusimageattributes.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Gdiplus.dll
api_name:
- ImageAttributes.GetLastStatus
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# ImageAttributes::GetLastStatus


## -description


The <b>ImageAttributes::GetLastStatus</b> method returns a value that indicates the nature of this <a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object's most recent method failure.


## -parameters






## -returns



Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

The <b>ImageAttributes::GetLastStatus</b> method returns an element of the <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If no methods invoked on this 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object have failed since the previous call to <b>ImageAttributes::GetLastStatus</b>, then <b>ImageAttributes::GetLastStatus</b> returns <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a>.

If at least one method invoked on this 
						<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object has failed since the previous call to <b>ImageAttributes::GetLastStatus</b>, then <b>ImageAttributes::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>ImageAttributes::GetLastStatus</b> immediately after constructing an 
				<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object to determine whether the constructor succeeded.

The first time you call the <b>ImageAttributes::GetLastStatus</b> method of an 
				<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a> object, it returns <a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Ok</a> if the constructor succeeded and all methods invoked so far on the 
				<b>ImageAttributes</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusimageattributes/nl-gdiplusimageattributes-imageattributes">ImageAttributes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplustypes/ne-gdiplustypes-status">Status</a>
 

 

