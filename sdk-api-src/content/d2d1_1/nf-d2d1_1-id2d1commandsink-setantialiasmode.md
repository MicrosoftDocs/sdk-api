---
UID: NF:d2d1_1.ID2D1CommandSink.SetAntialiasMode
title: ID2D1CommandSink::SetAntialiasMode
author: windows-sdk-content
description: Sets the antialiasing mode that will be used to render any subsequent geometry.
old-location: direct2d\id2d1commandsink_setantialiasmode.htm
tech.root: direct2d
ms.assetid: 335cb9e7-56da-4971-b6d1-94292a6a771a
ms.author: windowssdkdev
ms.date: 09/21/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetAntialiasMode method, ID2D1CommandSink.SetAntialiasMode, ID2D1CommandSink::SetAntialiasMode, SetAntialiasMode, SetAntialiasMode method [Direct2D], SetAntialiasMode method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetAntialiasMode, direct2d.id2d1commandsink_setantialiasmode
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
 - ID2D1CommandSink.SetAntialiasMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1CommandSink::SetAntialiasMode


## -description


Sets the antialiasing mode that will be used to render any subsequent geometry.


## -parameters




### -param antialiasMode

Type: <b><a href="https://msdn.microsoft.com/3ca12155-6dd0-41bb-8778-3387422c4ffe">D2D1_ANTIALIAS_MODE</a></b>

The antialiasing mode selected for the command list.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code. 





## -see-also




<a href="https://msdn.microsoft.com/52e6da86-c7c6-48e7-b0ff-a54770663f14">ID2D1CommandList::Stream</a>



<a href="https://msdn.microsoft.com/4e0ce837-7f4e-4b93-8dd7-68f60cfb1105">ID2D1CommandSink</a>



<a href="https://msdn.microsoft.com/cd727271-1725-48e1-be39-680b363db2ae">ID2D1RenderTarget::SetAntialiasMode</a>
 

 

