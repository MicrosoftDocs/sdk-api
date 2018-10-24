---
UID: NF:gdiplusstringformat.StringFormat.SetAlignment
title: StringFormat::SetAlignment
author: windows-sdk-content
description: The StringFormat::SetAlignment method sets the character alignment of this StringFormat object in relation to the origin of the layout rectangle. A layout rectangle is used to position the displayed string.
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetAlignment_align_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\setalignment_24align.htm
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: SetAlignment, SetAlignment method [GDI+], SetAlignment method [GDI+],StringFormat class, StringFormat class [GDI+],SetAlignment method, StringFormat.SetAlignment, StringFormat::SetAlignment, _gdiplus_CLASS_StringFormat_SetAlignment_align_, gdiplus._gdiplus_CLASS_StringFormat_SetAlignment_align_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusstringformat.h
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
 - StringFormat.SetAlignment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# StringFormat::SetAlignment


## -description


The <b>StringFormat::SetAlignment</b> method sets the character alignment of this 
			<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a> object in relation to the origin of the layout rectangle. A layout rectangle is used to position the displayed string. 


## -parameters




### -param align [in]

Type: <b><a href="https://msdn.microsoft.com/d395f6b4-8d8a-41b1-9c49-6fc2f005ca5d">StringAlignment</a></b>

Element of the <a href="https://msdn.microsoft.com/d395f6b4-8d8a-41b1-9c49-6fc2f005ca5d">StringAlignment</a> enumeration that specifies how a string is aligned in reference to the bounding rectangle. 


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If the method succeeds, it returns Ok, which is an element of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/dd8af524-688c-44dd-b3e4-deadb874bdc3">Font</a>



<a href="https://msdn.microsoft.com/6821442b-d352-48cb-a48a-839105a8c36a">RectF</a>



<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a>



<a href="https://msdn.microsoft.com/d395f6b4-8d8a-41b1-9c49-6fc2f005ca5d">StringAlignment</a>



<a href="https://msdn.microsoft.com/2d7af5fe-f3e9-4db3-90a5-4e623d9ce773">StringFormat</a>
 

 

