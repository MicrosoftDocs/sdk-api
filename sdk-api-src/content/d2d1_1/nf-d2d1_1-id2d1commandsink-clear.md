---
UID: NF:d2d1_1.ID2D1CommandSink.Clear
title: ID2D1CommandSink::Clear
author: windows-sdk-content
description: Clears the drawing area to the specified color.
old-location: direct2d\id2d1commandsink_clear.htm
tech.root: direct2d
ms.assetid: d91bb6b2-ecc8-4c16-95fc-c0cb7bbe80e3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Clear, Clear method [Direct2D], Clear method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],Clear method, ID2D1CommandSink.Clear, ID2D1CommandSink::Clear, d2d1_1/ID2D1CommandSink::Clear, direct2d.id2d1commandsink_clear
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandSink.Clear
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::Clear


## -description


Clears the drawing area to the specified color. 




## -parameters




### -param color

TBD




#### - clearColor [in, optional]

Type: <b>const <a href="https://msdn.microsoft.com/564d4f41-2da7-49ed-b85a-d1070d662b40">D2D1_COLOR_F</a>*</b>

The color to which the command sink should be cleared.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -remarks



The clear color is restricted by the currently selected clip and layer bounds.

If no color is specified, the color should be interpreted by context. Examples include but are not limited to:

<ul>
<li>Transparent black for a premultiplied bitmap target.</li>
<li>Opaque black for an ignore bitmap target.</li>
<li>Containing no content (or white) for a printer page.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/3bfec923-17fc-479a-a760-9baab2ff3a56">ID2D1RenderTarget::Clear</a>
 

 

