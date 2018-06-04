---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IRdcGeneratorParameters interface


## -description


The <b>IRdcGeneratorParameters</b> interface 
    is the generic interface for all types of generator parameters. All generator parameter objects must 
    support this interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IRdcGeneratorParameters</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IRdcGeneratorParameters</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IRdcGeneratorParameters</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9fd60d5-a542-4a00-becd-85c7dafbe105">GetGeneratorParametersType</a>
</td>
<td align="left" width="63%">
Returns the specific type of the parameters.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/58050740-0508-4797-b1b5-7a1e2a6dc00b">GetParametersVersion</a>
</td>
<td align="left" width="63%">
Returns information about the version of RDC used to serialize the parameters.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ebd41d6c-c321-4017-bcc1-a2cdf5202730">GetSerializeSize</a>
</td>
<td align="left" width="63%">
Returns the size, in bytes, of the serialized parameter data.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba0d09b0-417f-494a-a5e8-dccd08e5280a">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the parameter data into a block of memory.</p> (Inherited from <b>IRdcGeneratorParameters</b>)</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/a3131654-e849-4a88-acec-c49a61653bad">Remote Differential Compression Interfaces</a>
 

 

