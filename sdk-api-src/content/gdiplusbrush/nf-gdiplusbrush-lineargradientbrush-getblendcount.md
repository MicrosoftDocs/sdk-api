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
			<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object.


## -parameters






## -returns



Type: <strong>Type: <b>INT</b>
</strong>

This method returns the number of blend factors currently set for this 
						<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a> object. If no custom blend has been set by using <a href="https://msdn.microsoft.com/e2b96c7b-083c-47ef-9b29-3ec403f41462">LinearGradientBrush::SetBlend</a>, or if invalid positions were passed to <b>LinearGradientBrush::SetBlend</b>, then <a href="https://msdn.microsoft.com/2eadd02c-75fd-4317-a925-68a5d32b139e">LinearGradientBrush::GetBlend</a> returns 1.




## -see-also




<a href="https://msdn.microsoft.com/889558d5-9181-43ff-b862-e92966324208">Brushes and Filled Shapes</a>



<a href="https://msdn.microsoft.com/e37b4c3a-b753-483a-990f-da3bcc70acf5">Filling Shapes with a Gradient Brush</a>



<a href="https://msdn.microsoft.com/7aa94b39-bd4c-4e66-b0dc-77f8953797b1">Filling a Shape with a Color Gradient</a>



<a href="https://msdn.microsoft.com/43901cd3-b059-4830-9063-e8287899e18a">LinearGradientBrush</a>



<a href="https://msdn.microsoft.com/2eadd02c-75fd-4317-a925-68a5d32b139e">LinearGradientBrush::GetBlend</a>



<a href="https://msdn.microsoft.com/e2b96c7b-083c-47ef-9b29-3ec403f41462">LinearGradientBrush::SetBlend</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">Point</a>
 

 

