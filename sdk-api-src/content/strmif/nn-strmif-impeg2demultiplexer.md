---
UID: NN:strmif.IMpeg2Demultiplexer
title: IMpeg2Demultiplexer
author: windows-sdk-content
description: This interface is implemented on the MPEG-2 Demultiplexer filter (Demux) and is used in both program stream mode and transport stream mode.
old-location: dshow\impeg2demultiplexer.htm
tech.root: DirectShow
ms.assetid: e9242b96-0fc3-428e-b7ee-91a4f5e67305
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: IMpeg2Demultiplexer, IMpeg2Demultiplexer interface [DirectShow], IMpeg2Demultiplexer interface [DirectShow],described, IMpeg2DemultiplexerInterface, dshow.impeg2demultiplexer, strmif/IMpeg2Demultiplexer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - IMpeg2Demultiplexer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMpeg2Demultiplexer interface


## -description



This interface is implemented on the <a href="https://msdn.microsoft.com/99bfc55d-6519-4e85-98ce-cad27bd71ffb">MPEG-2 Demultiplexer</a> filter (Demux) and is used in both program stream mode and transport stream mode. It is called by applications or other filters to create, configure and delete output pins on the Demux. This interface is not exposed when the filter is playing back a file (pull-mode).




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMpeg2Demultiplexer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMpeg2Demultiplexer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMpeg2Demultiplexer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb863b9c-e8da-444a-b50f-37f4fe9d8164">CreateOutputPin</a>
</td>
<td align="left" width="63%">
Creates a new output pin on the Demux.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6c6a0e38-54b8-4fa3-b37a-00073d40965d">DeleteOutputPin</a>
</td>
<td align="left" width="63%">
Deletes the specified output pin.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/985033ea-72ea-40c4-8176-60208b505040">SetOutputPinMediaType</a>
</td>
<td align="left" width="63%">
Updates the media type of the specified output pin. (DirectX® 9.0 and later.)

</td>
</tr>
</table> 

