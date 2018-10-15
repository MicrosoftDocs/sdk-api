---
UID: NF:windows.media.streaming.IMediaRenderer.add_RenderingParametersUpdate
title: IMediaRenderer::streaming
author: windows-sdk-content
description: Registers an event handler for the RenderingParametersUpdate event.
old-location: mediastreaming\imediarenderer_add_renderingparametersupdate.htm
tech.root: mediastreaming
ms.assetid: 3CEED740-19EA-4CC6-B3F8-F9DE9C6DCC58
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: IMediaRenderer interface [Media Streaming API],add_RenderingParametersUpdate method, IMediaRenderer.add_RenderingParametersUpdate, IMediaRenderer.streaming, IMediaRenderer::add_RenderingParametersUpdate, IMediaRenderer::streaming, add_RenderingParametersUpdate, add_RenderingParametersUpdate method [Media Streaming API], add_RenderingParametersUpdate method [Media Streaming API],IMediaRenderer interface, mediastreaming.imediarenderer_add_renderingparametersupdate, windows/IMediaRenderer::add_RenderingParametersUpdate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: windows.media.streaming.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - windows.media.streaming.h
api_name:
 - IMediaRenderer.add_RenderingParametersUpdate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMediaRenderer::streaming


## -description


Registers an event handler for the <a href="https://msdn.microsoft.com/863CA879-A420-43D6-9AC8-94F8303BB759">RenderingParametersUpdate</a> event.


## -parameters




### -param handler [in]

A <a href="https://msdn.microsoft.com/e5e1659b-5b4b-4882-be89-4dc05c56d9f2">RenderingParametersUpdateHandler</a> event handler function.


### -param token [out, retval]

Reference to a token that can be used to unregister the event handler.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



To unregister the event handler that was registered by this method, pass the <i>token</i> value to the <a href="https://msdn.microsoft.com/5642D180-7FE8-4058-B346-109D5C5817F6">remove_RenderingParametersUpdate</a> method.




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

