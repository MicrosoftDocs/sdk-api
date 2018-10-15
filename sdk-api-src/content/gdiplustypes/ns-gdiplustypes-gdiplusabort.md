---
UID: NS:gdiplustypes.GdiplusAbort
title: GdiplusAbort
author: windows-sdk-content
description: The GdiplusAbort structure provides a mechanism that allows Windows GDI+ to call an application-defined Abort method periodically during time-consuming rendering operations.
old-location: gdiplus\_gdiplus_STRUC_GdiplusAbort.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\gdiplusabort.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: GdiplusAbort, GdiplusAbort structure [GDI+], _gdiplus_STRUC_GdiplusAbort, gdiplus._gdiplus_STRUC_GdiplusAbort, gdiplustypes/GdiplusAbort
ms.prod: windows
ms.technology: windows-sdk
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - GdiplusTypes.h
api_name:
 - GdiplusAbort
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<li>Pass the address of the <b>GdiplusAbort</b> descendant to the <a href="https://msdn.microsoft.com/en-us/library/ms535403(v=VS.85).aspx">Image::SetAbort</a> method.</li>
</ol>
During certain time-consuming rendering operations (for example, a call to the <a href="https://msdn.microsoft.com/en-us/library/ms535746(v=VS.85).aspx">Graphics::DrawImage</a> method), GDI+ calls the <b>Abort</b> method periodically. For some operations the callback is every 250 milliseconds; for other operations the callback is not based on a timer. If the <b>Abort</b> method returns S_OK, GDI+ continues the rendering operation. If the <b>Abort</b> method returns E_ABORT, GDI+ aborts the rendering operation.



