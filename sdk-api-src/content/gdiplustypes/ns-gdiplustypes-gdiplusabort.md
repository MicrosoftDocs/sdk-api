---
UID: NS:gdiplustypes.GdiplusAbort
title: GdiplusAbort
author: windows-driver-content
description: The GdiplusAbort structure provides a mechanism that allows Windows GDI+ to call an application-defined Abort method periodically during time-consuming rendering operations.
old-location: gdiplus\_gdiplus_STRUC_GdiplusAbort.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\gdiplusabort.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: GdiplusAbort, GdiplusAbort structure [GDI+], _gdiplus_STRUC_GdiplusAbort, gdiplus._gdiplus_STRUC_GdiplusAbort, gdiplustypes/GdiplusAbort
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: gdiplustypes.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	GdiplusTypes.h
api_name:
-	GdiplusAbort
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# GdiplusAbort structure


## -description


The <b>GdiplusAbort</b> structure provides a mechanism that allows Windows GDI+ to call an application-defined <b>Abort</b> method periodically during time-consuming rendering operations.


## -struct-fields


## -remarks



The <b>GdiplusAbort</b> structure has only one method, a virtual method named <b>Abort</b>. The <b>GdiplusAbort</b> structure has no data members.

To create a callback method, follow these steps.

<ol>
<li>
Create a structure that descends from <b>GdiplusAbort</b>, and implement the following method.

<code>HRESULT __stdcall Abort(void)</code>

</li>
<li>Create data members to hold any data that will be needed by the <b>Abort</b> method.</li>
<li>Pass the address of the <b>GdiplusAbort</b> descendant to the <a href="https://msdn.microsoft.com/2df54a2c-cb7b-4d65-a27d-7342e00ed71b">Image::SetAbort</a> method.</li>
</ol>
During certain time-consuming rendering operations (for example, a call to the <a href="https://msdn.microsoft.com/c9577988-e52f-4f71-ab1b-51bb5368812e">Graphics::DrawImage</a> method), GDI+ calls the <b>Abort</b> method periodically. For some operations the callback is every 250 milliseconds; for other operations the callback is not based on a timer. If the <b>Abort</b> method returns S_OK, GDI+ continues the rendering operation. If the <b>Abort</b> method returns E_ABORT, GDI+ aborts the rendering operation.



