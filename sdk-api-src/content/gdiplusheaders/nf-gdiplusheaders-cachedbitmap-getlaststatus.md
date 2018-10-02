---
UID: NF:gdiplusheaders.CachedBitmap.GetLastStatus
title: CachedBitmap::GetLastStatus
author: windows-sdk-content
description: The CachedBitmap::GetLastStatus method returns a value that indicates whether this CachedBitmap object was constructed successfully.
old-location: gdiplus\_gdiplus_CLASS_CachedBitmap_GetLastStatus_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\cachedbitmapclass\getlaststatus_27.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CachedBitmap class [GDI+],GetLastStatus method, CachedBitmap.GetLastStatus, CachedBitmap::GetLastStatus, GetLastStatus, GetLastStatus method [GDI+], GetLastStatus method [GDI+],CachedBitmap class, _gdiplus_CLASS_CachedBitmap_GetLastStatus_, gdiplus._gdiplus_CLASS_CachedBitmap_GetLastStatus_
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gdiplusheaders.h
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
 - CachedBitmap.GetLastStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# CachedBitmap::GetLastStatus


## -description


The <b>CachedBitmap::GetLastStatus</b> method returns a value that indicates whether this 
			<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object was constructed successfully.


## -parameters






## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a></b>
</strong>

If this 
						<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object was constructed successfully, the 
						<b>CachedBitmap::GetLastStatus</b> method returns <a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Ok</a>, which is an element of the 
						<b>Status</b> enumeration.

If this 
						<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a> object was not constructed successfully, the <b>CachedBitmap::GetLastStatus</b> method returns an element of the 
						<a href="https://msdn.microsoft.com/035fb1bb-cdf3-47e5-a4c7-024598fa01a3">Status</a> enumeration that indicates the nature of the failure.




## -see-also




<a href="https://msdn.microsoft.com/f9826772-bb8a-4339-9cea-f77637f971b2">Bitmap</a>



<a href="https://msdn.microsoft.com/298880a5-cc6a-4b1a-9459-7cf6c2252328">CachedBitmap</a>



<a href="https://msdn.microsoft.com/7e874710-3cd3-42c8-bd2f-8a779b19ba59">Graphics</a>



<a href="https://msdn.microsoft.com/3732095d-c812-4ce5-80f1-9b191b4ff01c">Image</a>



<a href="https://msdn.microsoft.com/42e2b664-197c-4c54-9220-b6231d6439d0">Using a Cached Bitmap to Improve Performance</a>
 

 

