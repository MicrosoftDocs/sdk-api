---
UID: NF:d2d1_1.ID2D1CommandSink.EndDraw
title: ID2D1CommandSink::EndDraw
author: windows-sdk-content
description: Indicates when ID2D1CommandSink processing has completed.
old-location: direct2d\id2d1commandsink_enddraw.htm
tech.root: direct2d
ms.assetid: 7324d66b-b415-4e07-9fe3-d79a1c0a49b0
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: EndDraw, EndDraw method [Direct2D], EndDraw method [Direct2D],ID2D1CommandSink interface, ID2D1CommandSink interface [Direct2D],EndDraw method, ID2D1CommandSink.EndDraw, ID2D1CommandSink::EndDraw, d2d1_1/ID2D1CommandSink::EndDraw, direct2d.id2d1commandsink_enddraw
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
 - ID2D1CommandSink.EndDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::EndDraw


## -description


Indicates when  <a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a> processing has completed.


## -parameters






## -returns



Type: <b>HRESULT</b>

If the method/function succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



The <b>HRESULT</b> active at the end of the command list will be returned.

 It allows the calling function or method to indicate a failure back to the stream implementation.




## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">ID2D1RenderTarget::EndDraw</a>
 

 

