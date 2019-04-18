---
UID: NN:tapi3if.ITSubStream
title: ITSubStream (tapi3if.h)
author: windows-sdk-content
description: An ITSubStream is a component of an ITStream, and gives an application finer control over the media streaming.
old-location: tapi3\itsubstream.htm
tech.root: Tapi
ms.assetid: fc495bc3-1172-4e39-b617-055b7ac95898
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITSubStream, ITSubStream interface [TAPI 2.2], ITSubStream interface [TAPI 2.2],described, _tapi3_itsubstream, tapi3.itsubstream, tapi3if/ITSubStream
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
 - ITSubStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITSubStream interface


## -description


An 
<b>ITSubStream</b> is a component of an 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>, and gives an application finer control over the media streaming. The 
<b>ITSubStream</b> interface provides methods that start, pause, or stop a substream, select or unselect terminals, and obtain a list of terminals selected on the stream. The 
<a href="https://msdn.microsoft.com/fa8c4017-09ac-44e9-a7fa-922d0588d92a">IEnumSubStream::Next</a> and 
<a href="https://msdn.microsoft.com/00fe0f8f-c814-4ae6-a60b-c58f3dc60b67">ITSubStreamControl::CreateSubStream</a> methods create the 
<b>ITSubStream</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSubStream</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITSubStream</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSubStream</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bf5e1f7f-3820-433e-b71f-53798c202593">EnumerateTerminals</a>
</td>
<td align="left" width="63%">
Enumerates terminals selected on the substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ec97e621-3789-46a4-b6b6-96639c5e7d4f">get_Stream</a>
</td>
<td align="left" width="63%">
Retrieves pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface for current substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/100854aa-78de-4395-9081-3b1f845c254c">get_Terminals</a>
</td>
<td align="left" width="63%">
Creates a collection of terminals associated with the current substream. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77bd3726-3996-45a6-88be-cb033f5dddc0">PauseSubStream</a>
</td>
<td align="left" width="63%">
Pauses the substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dc558ab-7422-4106-831e-9d2812530e0a">SelectTerminal</a>
</td>
<td align="left" width="63%">
Selects an 
<a href="https://msdn.microsoft.com/38bc30fa-3e4e-417a-9d04-931ba2451fa4">ITTerminal</a> object onto the substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/603cb667-a108-4e47-9808-99fddad5d894">StartSubStream</a>
</td>
<td align="left" width="63%">
Starts the substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa5028f6-80eb-4076-a81c-c83b462fc27c">StopSubStream</a>
</td>
<td align="left" width="63%">
Stops the substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1b84377-bb1f-4e88-aca5-91105ff2ad6a">UnselectTerminal</a>
</td>
<td align="left" width="63%">
Unselects the terminal from the substream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a>



<a href="https://msdn.microsoft.com/17c5f2ba-d526-4b00-9649-8fd73d70bc79">ITSubStreamControl</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

