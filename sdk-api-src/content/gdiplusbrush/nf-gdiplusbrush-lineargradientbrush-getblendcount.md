---
UID: NF:gdiplusbrush.LinearGradientBrush.GetBlendCount
title: LinearGradientBrush::GetBlendCount
author: windows-sdk-content
description: The LinearGradientBrush::GetBlendCount method gets the number of blend factors currently set for this LinearGradientBrush object.
old-location: gdiplus\_gdiplus_CLASS_LinearGradientBrush_GetBlendCount_.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\lineargradientbrushclass\lineargradientbrushmethods\getblendcount.htm
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: GetBlendCount, GetBlendCount method [GDI+], GetBlendCount method [GDI+],LinearGradientBrush class, LinearGradientBrush class [GDI+],GetBlendCount method, LinearGradientBrush.GetBlendCount, LinearGradientBrush::GetBlendCount, _gdiplus_CLASS_LinearGradientBrush_GetBlendCount_, gdiplus._gdiplus_CLASS_LinearGradientBrush_GetBlendCount_
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: KnownGamingPrivileges
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - LinearGradientBrush.GetBlendCount
product: Windows
targetos: Windows
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
req.product: GDI+ 1.0
---

# LinearGradientBrush::GetBlendCount


## -description


The <b>LinearGradientBrush::GetBlendCount</b> method gets the number of blend factors currently set for this 
			<a href="https://msdn.microsoft.com/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a> object.


## -parameters






## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of blend factors currently set for this 
						<a href="https://msdn.microsoft.com/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a> object. If no custom blend has been set by using <a href="https://msdn.microsoft.com/library/ms535342(v=VS.85).aspx">LinearGradientBrush::SetBlend</a>, or if invalid positions were passed to <b>LinearGradientBrush::SetBlend</b>, then <a href="https://msdn.microsoft.com/library/ms535328(v=VS.85).aspx">LinearGradientBrush::GetBlend</a> returns 1.




## -see-also




<a href="https://msdn.microsoft.com/library/ms536356(v=VS.85).aspx">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/library/ms533806(v=VS.85).aspx">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/library/ms533856(v=VS.85).aspx">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/library/ms534473(v=VS.85).aspx">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/library/ms535328(v=VS.85).aspx">LinearGradientBrush::GetBlend</a>



<a href="https://msdn.microsoft.com/library/ms535342(v=VS.85).aspx">LinearGradientBrush::SetBlend</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a>
 

 

