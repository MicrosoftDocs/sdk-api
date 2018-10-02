---
UID: NF:strmif.IFilterGraph2.RenderEx
title: IFilterGraph2::RenderEx
author: windows-sdk-content
description: The RenderEx method renders an output pin, with an option to use existing renderers only.
old-location: dshow\ifiltergraph2_renderex.htm
tech.root: DirectShow
ms.assetid: b169c784-2ce3-47dc-ad64-3e4c96483f34
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IFilterGraph2 interface [DirectShow],RenderEx method, IFilterGraph2.RenderEx, IFilterGraph2::RenderEx, IFilterGraph2RenderEx, RenderEx, RenderEx method [DirectShow], RenderEx method [DirectShow],IFilterGraph2 interface, dshow.ifiltergraph2_renderex, strmif/IFilterGraph2::RenderEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFilterGraph2.RenderEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFilterGraph2::RenderEx


## -description



The <code>RenderEx</code> method renders an output pin, with an option to use existing renderers only.




## -parameters




### -param pPinOut [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of the output pin.


### -param dwFlags [in]

Flag that specifies how to render the pin. If the value is AM_RENDEREX_RENDERTOEXISTINGRENDERERS, the method attempts to use renderers already in the filter graph. It will not add new renderers to the graph. (It will add intermediate transform filters, if needed.) For the method to succeed, the graph must contain the appropriate renderers, and they must have unconnected input pins. If the value is zero, the method behaves identically to the <a href="https://msdn.microsoft.com/de3adac7-ff99-4415-9afc-e25ad420df59">IGraphBuilder::Render</a> method.


### -param pvContext [in, out]

Reserved. Must be <b>NULL</b>.


## -returns



Returns an <b>HRESULT</b>.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/1a1ef4fe-a054-4ba7-99c7-1f209472c5a6">IFilterGraph2 Interface</a>
 

 

