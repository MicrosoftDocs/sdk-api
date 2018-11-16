---
UID: NN:tapi3if.ITSubStreamControl
title: ITSubStreamControl
author: windows-sdk-content
description: The ITSubStreamControl interface exposes methods that allow an application to enumerate, create, or remove substreams. Many MSPs do not support this interface.
old-location: tapi3\itsubstreamcontrol.htm
tech.root: Tapi
ms.assetid: 17c5f2ba-d526-4b00-9649-8fd73d70bc79
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITSubStreamControl, ITSubStreamControl interface [TAPI 2.2], ITSubStreamControl interface [TAPI 2.2],described, _tapi3_itsubstreamcontrol, tapi3.itsubstreamcontrol, tapi3if/ITSubStreamControl
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITSubStreamControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITSubStreamControl interface


## -description


The 
<b>ITSubStreamControl</b> interface exposes methods that allow an application to enumerate, create, or remove substreams. Many MSPs do not support this interface.

A pointer to this interface can be obtained by calling <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> on the stream object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITSubStreamControl</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITSubStreamControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITSubStreamControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/00fe0f8f-c814-4ae6-a60b-c58f3dc60b67">CreateSubStream</a>
</td>
<td align="left" width="63%">
Creates a substream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/848d31e8-f878-4d33-b2b9-2d28e96bd14a">EnumerateSubStreams</a>
</td>
<td align="left" width="63%">
Enumerates substreams.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ea7dca0-9a0b-4966-83ba-0d1f6c5e5ccb">get_SubStreams</a>
</td>
<td align="left" width="63%">
Creates a collection of substreams associated with the current stream. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a1be17c-2cae-4eea-a20a-3344915c5234">RemoveSubStream</a>
</td>
<td align="left" width="63%">
Removes a substream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/12b9457a-7afb-4348-93a2-28728c673929">ITStreamControl</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

