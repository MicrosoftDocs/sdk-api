---
UID: NF:windows.media.streaming.IMediaRenderer.remove_TransportParametersUpdate
title: IMediaRenderer::remove_TransportParametersUpdate method
author: windows-driver-content
description: Unregisters an event handler for the TransportParametersUpdate event.
old-location: mediastreaming\imediarenderer_remove_transportparametersupdate.htm
old-project: mediastreaming
ms.assetid: 7AA7B336-5C51-4774-89A1-F710603A7B23
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IMediaRenderer, IMediaRenderer interface [Media Streaming API], remove_TransportParametersUpdate method, IMediaRenderer::remove_TransportParametersUpdate, mediastreaming.imediarenderer_remove_transportparametersupdate, remove_TransportParametersUpdate method [Media Streaming API], remove_TransportParametersUpdate method [Media Streaming API], IMediaRenderer interface, remove_TransportParametersUpdate,IMediaRenderer.remove_TransportParametersUpdate, windows/IMediaRenderer::remove_TransportParametersUpdate
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
req.typenames: PDF_RENDER_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	windows.media.streaming.h
api_name:
-	IMediaRenderer.remove_TransportParametersUpdate
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IMediaRenderer::remove_TransportParametersUpdate method


## -description


Unregisters an event handler for the <a href="https://msdn.microsoft.com/DF9256CA-6C59-462C-B32F-4653546DB384">TransportParametersUpdate</a> event.


## -parameters




### -param token [in]

A reference to a token obtained from the <a href="https://msdn.microsoft.com/34D11925-387B-414F-A176-336BBCF87821">add_TransportParametersUpdate</a> method when the event handler was registered.


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
 




## -see-also




<a href="https://msdn.microsoft.com/FBA5BF5A-FA5A-4E25-8F2B-9D1C0A9BCACB">IMediaRenderer</a>
 

 

