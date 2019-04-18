---
UID: NN:dvbsiparser.IDvbComponentDescriptor
title: IDvbComponentDescriptor (dvbsiparser.h)
author: windows-sdk-content
description: Identifies the type of a Digital Video Broadcast (DVB) component stream and provides a text description of the component stream.
old-location: mstv\idvbcomponentdescriptor.htm
tech.root: mstv
ms.assetid: 0dee15ee-5b36-4454-8092-6b57ef5063ce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDvbComponentDescriptor, IDvbComponentDescriptor interface [Microsoft TV Technologies], IDvbComponentDescriptor interface [Microsoft TV Technologies],described, dvbsiparser/IDvbComponentDescriptor, mstv.idvbcomponentdescriptor
ms.topic: interface
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - dvbsiparser.h
api_name:
 - IDvbComponentDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbComponentDescriptor interface


## -description


Identifies the type of a Digital Video Broadcast (DVB) component stream and provides a text description of the component stream.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDvbComponentDescriptor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDvbComponentDescriptor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDvbComponentDescriptor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1ecfb7db-2fb6-4389-8f62-3d912ffc301b">GetComponentTag</a>
</td>
<td align="left" width="63%">
Gets the component tag from  a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7bf5e21-1c88-4b5e-b043-33a127fad65f">GetComponentType</a>
</td>
<td align="left" width="63%">
 Gets the component type code for a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9898cd33-db5d-41d3-9e3d-77da2ff38e44">GetLanguageCode</a>
</td>
<td align="left" width="63%">
Gets the ISO 639 language identifier for a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/418d654a-a8cf-42f1-b361-bc1bf80da194">GetLength</a>
</td>
<td align="left" width="63%">
Gets the body length of a  a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3bfa86c4-2b94-43cd-842e-33cc03b713a5">GetStreamContent</a>
</td>
<td align="left" width="63%">
 Gets the stream content code for a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/680be3c5-ed02-4719-a510-cf84615f8738">GetTag</a>
</td>
<td align="left" width="63%">
Gets the tag that identifies a DVB component descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b4ff757-24d0-4dca-8def-c8079724e571">GetTextW</a>
</td>
<td align="left" width="63%">
 Gets the text describing the elementary stream  from a DVB component descriptor, in Unicode string format.

</td>
</tr>
</table> 

