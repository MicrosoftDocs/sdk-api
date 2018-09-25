---
UID: NF:gdiplusinit.GdiplusShutdown
title: GdiplusShutdown function
author: windows-sdk-content
description: The GdiplusShutdown function cleans up resources used by Windows GDI+. Each call to GdiplusStartup should be paired with a call to GdiplusShutdown.
old-location: gdiplus\_gdiplus_FUNC_GdiplusShutdown_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\functions\gdiplusshutdown.htm
ms.author: windowssdkdev
ms.date: 09/12/2018
ms.keywords: GdiplusShutdown, GdiplusShutdown function [GDI+], _gdiplus_FUNC_GdiplusShutdown_, gdiplus._gdiplus_FUNC_GdiplusShutdown_, gdiplusinit/GdiplusShutdown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: gdiplusinit.h
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
 - DllExport
api_location:
 - Gdiplus.dll
api_name:
 - GdiplusShutdown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
---

# GdiplusShutdown function


## -description


The <b>GdiplusShutdown</b> function cleans up resources used by Windows GDI+. Each call to <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a> should be paired with a call to <b>GdiplusShutdown</b>.


## -parameters




### -param token [in]

Type: <b>ULONG_PTR</b>

Token returned by a previous call to <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a>. 


## -returns



This function does not return a value.




## -remarks



You must call <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a> before you create any GDI+ objects, and you must delete all of your GDI+ objects (or have them go out of scope) before you call <b>GdiplusShutdown</b>.

<div class="alert"><b>Note</b>  For Windows 7 and earlier, if GDI+ can't create a font family, it substitutes the generic Sans Serif family and client-side caches the pointer for the generic family. Because calls to <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a> and <b>GdiplusShutdown</b> are not aware of this caching, the operating system retains the pointer for the generic family object past the object's lifetime, which causes the operating system to crash. For Windows 8 and later, GDI+ returns a sentinel value for the generic family object that remains constant across calls to <b>GdiplusStartup</b> and <b>GdiplusShutdown</b> so the operating system doesn't retain the pointer for the generic family object past the object's lifetime.</div>
<div> </div>

#### Examples

For an example of calling <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a> and <b>GdiplusShutdown</b>, see <a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3748a252-db65-4471-8345-ab0c136c5a21">GdiplusStartup</a>



<a href="https://msdn.microsoft.com/dd0ffdd3-f05c-4ad4-a7c8-727d1d3ec83c">GdiplusStartupInput</a>



<a href="https://msdn.microsoft.com/dcf89c6f-c0b2-4df0-910c-43d8d758fbaf">GdiplusStartupOutput</a>



<a href="https://msdn.microsoft.com/c03c5ef1-13f6-4cf5-9395-be90b46aa6bb">Getting Started</a>
 

 

