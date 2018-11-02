---
UID: NN:tapi3if.ITStreamControl
title: ITStreamControl
author: windows-sdk-content
description: The ITStreamControl interface represents the media streaming features of a call and exposes methods that allow an application to enumerate, create, or remove streams.
old-location: tapi3\itstreamcontrol.htm
tech.root: tapi
ms.assetid: 12b9457a-7afb-4348-93a2-28728c673929
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: ITStreamControl, ITStreamControl interface [TAPI 2.2], ITStreamControl interface [TAPI 2.2],described, _tapi3_itstreamcontrol, tapi3.itstreamcontrol, tapi3if/ITStreamControl
ms.prod: windows
ms.technology: windows-sdk
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
 - ITStreamControl
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITStreamControl interface


## -description


The 
<b>ITStreamControl</b> interface represents the media streaming features of a call and exposes methods that allow an application to enumerate, create, or remove streams.

If this interface exists, a TAPI application acquires a pointer to this interface by performing a <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> on any call interface, such as 
<a href="https://msdn.microsoft.com/5209d4a1-e05b-453e-8896-2dc71f0b9af0">ITCallInfo</a>. This interface is not available if an MSP is not involved in the current call session.

Internal to the TAPI DLL, this interface is implemented by the MSP's call object, which is created in the 
<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">ITMSPAddress::CreateMSPCall</a> method. TAPI then aggregates this interface onto the TAPI call object and exposes it to TAPI applications.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITStreamControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITStreamControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITStreamControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/402cde43-6b2a-4e4e-bf46-97fcafb7574a">CreateStream</a>
</td>
<td align="left" width="63%">
Creates a media stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/de018f3e-d3b9-4093-a2b5-4929ac4d1d2a">EnumerateStreams</a>
</td>
<td align="left" width="63%">
Enumerates streams currently available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d001f5a-7731-47b9-8c68-e4dd2d0bf02f">get_Streams</a>
</td>
<td align="left" width="63%">
Creates a collection of streams currently available. Provided for Automation client applications, such as those written in Microsoft Visual Basic.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd432d49-04f6-4f1f-a6a1-937658d615d6">RemoveStream</a>
</td>
<td align="left" width="63%">
Removes a media stream.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a>



<a href="https://msdn.microsoft.com/fc495bc3-1172-4e39-b617-055b7ac95898">ITSubStream</a>



<a href="https://msdn.microsoft.com/17c5f2ba-d526-4b00-9649-8fd73d70bc79">ITSubStreamControl</a>



<a href="https://msdn.microsoft.com/53b7bcbd-571a-44da-a6db-10d4c3e5d30a">Media Service Provider Interface (MSPI)</a>
 

 

