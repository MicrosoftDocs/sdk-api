---
UID: NF:gdiplusimageattributes.ImageAttributes.GetLastStatus
title: ImageAttributes::GetLastStatus
author: windows-sdk-content
description: The ImageAttributes::GetLastStatus method returns a value that indicates the nature of this ImageAttributes object's most recent method failure.
old-location: gdiplus\_gdiplus_CLASS_ImageAttributes_GetLastStatus_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\imageattributesclass\imageattributesmethods\getlaststatus_2.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],ImageAttributes class, ImageAttributes class [GDI+],GetLastStatus method, ImageAttributes.GetLastStatus, ImageAttributes::GetLastStatus, _gdiplus_CLASS_ImageAttributes_GetLastStatus_, gdiplus._gdiplus_CLASS_ImageAttributes_GetLastStatus_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - ImageAttributes.GetLastStatus
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# ImageAttributes::GetLastStatus


## -description


The <b>ImageAttributes::GetLastStatus</b> method returns a value that indicates the nature of this <a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object's most recent method failure.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a></b>
</strong>

The <b>ImageAttributes::GetLastStatus</b> method returns an element of the <a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a> enumeration.

If no methods invoked on this 
						<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object have failed since the previous call to <b>ImageAttributes::GetLastStatus</b>, then <b>ImageAttributes::GetLastStatus</b> returns <a href="https://msdn.microsoft.com/library/ms534175(v=VS.85).aspx">Ok</a>.

If at least one method invoked on this 
						<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object has failed since the previous call to <b>ImageAttributes::GetLastStatus</b>, then <b>ImageAttributes::GetLastStatus</b> returns a value that indicates the nature of the most recent failure.




## -remarks



You can call <b>ImageAttributes::GetLastStatus</b> immediately after constructing an 
				<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object to determine whether the constructor succeeded.

The first time you call the <b>ImageAttributes::GetLastStatus</b> method of an 
				<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a> object, it returns <a href="https://msdn.microsoft.com/library/ms534175(v=VS.85).aspx">Ok</a> if the constructor succeeded and all methods invoked so far on the 
				<b>ImageAttributes</b> object succeeded. Otherwise, it returns a value that indicates the nature of the most recent failure.




## -see-also




<a href="https://msdn.microsoft.com/library/ms534464(v=VS.85).aspx">ImageAttributes</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>
 

 

