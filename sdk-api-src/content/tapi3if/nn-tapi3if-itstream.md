---
UID: NN:tapi3if.ITStream
title: ITStream
author: windows-sdk-content
description: The ITStream interfaces expose methods that allow an application to retrieve information on a stream; to start, pause, or stop the stream; to select or unselect terminals on a stream; and to obtain a list of terminals selected on the stream.
old-location: tapi3\itstream.htm
tech.root: Tapi
ms.assetid: 74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITStream, ITStream interface [TAPI 2.2], ITStream interface [TAPI 2.2],described, _tapi3_itstream, tapi3.itstream, tapi3if/ITStream
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITStream interface


## -description


The 
<b>ITStream</b> interfaces expose methods that allow an application to retrieve information on a stream; to start, pause, or stop the stream; to select or unselect terminals on a stream; and to obtain a list of terminals selected on the stream. The following methods create the 
<b>ITStream</b> interface:


<a href="https://msdn.microsoft.com/en-us/library/ms726500(v=VS.85).aspx">CMSPCallBase::CreateStreamObject</a>



<a href="https://msdn.microsoft.com/96399092-88fa-4b3c-aede-ee61c7c0320a">IEnumStream::Next</a>



<a href="https://msdn.microsoft.com/ec97e621-3789-46a4-b6b6-96639c5e7d4f">ITSubStream::get_Stream</a>



<a href="https://msdn.microsoft.com/402cde43-6b2a-4e4e-bf46-97fcafb7574a">ITStreamControl::CreateStream</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITStream</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITStream</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/c57af2a9-a2ec-45ba-9e10-7b5f41bdeb00">EnumerateTerminals</a>
</td>
<td align="left" width="63%">
Enumerates terminals selected on the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/196abe2a-d88d-4b2d-8867-4e6cc15dee33">get_Direction</a>
</td>
<td align="left" width="63%">
Gets the stream's 
<a href="https://msdn.microsoft.com/55ef9df3-1b85-439b-8ecb-28e5069390b9">terminal direction</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/871caaf3-12c4-457c-8d0f-0ee9be52a58b">get_MediaType</a>
</td>
<td align="left" width="63%">
Gets the stream's 
<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">media type</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3b81bd7-f99a-4cb1-8d60-6be8c1e68722">get_Name</a>
</td>
<td align="left" width="63%">
Gets a <b>BSTR</b> representing the name of the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2861dbf7-fc13-4182-90e5-32347f3d1e54">get_Terminals</a>
</td>
<td align="left" width="63%">
Creates a collection of terminals associated with the current stream. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7d70dd9-dcac-4b25-9954-10b4d6b436de">PauseStream</a>
</td>
<td align="left" width="63%">
Pauses the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ecc4c7eb-c278-457a-b54e-5f1e582e22bf">SelectTerminal</a>
</td>
<td align="left" width="63%">
Selects an 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> object onto the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/23553f00-5ce5-465e-b455-8bf2d73dae9d">StartStream</a>
</td>
<td align="left" width="63%">
Starts the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6014e76e-ce2c-4ab8-b6f2-c09fc2acf315">StopStream</a>
</td>
<td align="left" width="63%">
Stops the stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ad16ea41-0c02-4bba-bfd9-267b56c481e1">UnselectTerminal</a>
</td>
<td align="left" width="63%">
Unselects the terminal from the stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/17c5f2ba-d526-4b00-9649-8fd73d70bc79">ITSubStreamControl</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

