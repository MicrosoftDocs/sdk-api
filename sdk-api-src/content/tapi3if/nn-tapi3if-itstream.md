---
UID: NN:tapi3if.ITStream
title: ITStream (tapi3if.h)
description: The ITStream interfaces expose methods that allow an application to retrieve information on a stream; to start, pause, or stop the stream; to select or unselect terminals on a stream; and to obtain a list of terminals selected on the stream.helpviewer_keywords: ["ITStream","ITStream interface [TAPI 2.2]","ITStream interface [TAPI 2.2]","described","_tapi3_itstream","tapi3.itstream","tapi3if/ITStream"]
old-location: tapi3\itstream.htm
tech.root: Tapi
ms.assetid: 74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a
ms.date: 12/05/2018
ms.keywords: ITStream, ITStream interface [TAPI 2.2], ITStream interface [TAPI 2.2],described, _tapi3_itstream, tapi3.itstream, tapi3if/ITStream
f1_keywords:
- tapi3if/ITStream
dev_langs:
- c++
req.header: tapi3if.h
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
- Tapi3if.h
api_name:
- ITStream
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITStream interface


## -description


The 
<b>ITStream</b> interfaces expose methods that allow an application to retrieve information on a stream; to start, pause, or stop the stream; to select or unselect terminals on a stream; and to obtain a list of terminals selected on the stream. The following methods create the 
<b>ITStream</b> interface:


<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-createstreamobject">CMSPCallBase::CreateStreamObject</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-ienumstream-next">IEnumStream::Next</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-get_stream">ITSubStream::get_Stream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream">ITStreamControl::CreateStream</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITStream</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-enumerateterminals">EnumerateTerminals</a>
</td>
<td align="left" width="63%">
Enumerates terminals selected on the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-get_direction">get_Direction</a>
</td>
<td align="left" width="63%">
Gets the stream's 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">terminal direction</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-get_mediatype">get_MediaType</a>
</td>
<td align="left" width="63%">
Gets the stream's 
<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">media type</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets a <b>BSTR</b> representing the name of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-get_terminals">get_Terminals</a>
</td>
<td align="left" width="63%">
Creates a collection of terminals associated with the current stream. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-pausestream">PauseStream</a>
</td>
<td align="left" width="63%">
Pauses the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-selectterminal">SelectTerminal</a>
</td>
<td align="left" width="63%">
Selects an 
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a> object onto the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-startstream">StartStream</a>
</td>
<td align="left" width="63%">
Starts the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-stopstream">StopStream</a>
</td>
<td align="left" width="63%">
Stops the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nf-tapi3if-itstream-unselectterminal">UnselectTerminal</a>
</td>
<td align="left" width="63%">
Unselects the terminal from the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="https://docs.microsoft.com/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="https://docs.microsoft.com/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
 

 

