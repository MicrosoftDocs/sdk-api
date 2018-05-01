---
UID: NF:d2d1.Resize
title: Resize function
author: windows-driver-content
description: Changes the size of the render target to the specified pixel size.
old-location: direct2d\id2d1hwndrendertarget_resize.htm
old-project: Direct2D
ms.assetid: b8ea2e96-c69b-4018-9572-c9099bf6202d
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: Resize, Resize methods [Direct2D], d2d1/Resize, direct2d.id2d1hwndrendertarget_resize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D2D1_WINDOW_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	D2d1.dll
api_name:
-	ID2D1HwndRenderTarget::Resize
product: Windows
targetos: Windows
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
---

# Resize function


## -description


<span>Changes the size of the render target to the specified pixel size.
</span><h3>Overload list</h3><table>
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99cee6c1-3c0c-4a6d-ab58-a90fc502e8d5">Resize(D2D1_SIZE_U&)</a>
</td>
<td align="left" width="63%">
Changes the size of the render target to the specified pixel size.

</td>
</tr>
<tr>
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a1e7aae-9660-4c35-9d7b-374f3ff28253">Resize(D2D1_SIZE_U*)</a>
</td>
<td align="left" width="63%">

    Changes the size of the render target to the specified pixel size.

</td>
</tr>
</table>

## -parameters


## -remarks



After this method is called, the contents of the render target's back-buffer are not defined, even if the <a href="https://msdn.microsoft.com/56178ee9-7d35-42e1-97f8-62835010f277">D2D1_PRESENT_OPTIONS_RETAIN_CONTENTS</a> option was specified when the render target was created.




## -see-also




<a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a>
 

 

