---
UID: NN:mmdeviceapi.IMMEndpoint
title: IMMEndpoint
author: windows-sdk-content
description: The IMMEndpoint interface represents an audio endpoint device.
old-location: coreaudio\immendpoint.htm
old-project: CoreAudio
ms.assetid: 293de8eb-204a-4c18-807c-b1405db85b12
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IMMEndpoint, IMMEndpoint interface [Core Audio], IMMEndpoint interface [Core Audio],described, coreaudio.immendpoint, mmdeviceapi/IMMEndpoint
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mmdeviceapi.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EndpointFormFactor
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmdeviceapi.h
api_name:
 - IMMEndpoint
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmdevapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# IMMEndpoint interface


## -description



The <b>IMMEndpoint</b> interface represents an <a href="https://msdn.microsoft.com/773714fb-3b00-4f03-988f-05c5835f87cf">audio endpoint device</a>. A client obtains a reference to an <b>IMMEndpoint</b> interface instance by following these steps:

<ol>
<li>By using one of the techniques described in <a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>, obtain a reference to the <b>IMMDevice</b> interface of an audio endpoint device.</li>
<li>Call the <b>IMMDevice::QueryInterface</b> method with parameter <i>iid</i> set to <b>REFIID</b> IID_IMMEndpoint.</li>
</ol>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMMEndpoint</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMMEndpoint</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMMEndpoint</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/01882c44-bf0c-4180-846e-c1e98c6fb472">GetDataFlow</a>
</td>
<td align="left" width="63%">
Indicates whether the endpoint is associated with a rendering device or a capture device.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b18e2094-e974-4c23-b70b-ace5a168132d">Core Audio Interfaces</a>



<a href="https://msdn.microsoft.com/12b05e7e-81b2-49fd-bb9f-d5ad3315c580">IMMDevice Interface</a>



<a href="https://msdn.microsoft.com/3a8fd734-0761-4b5b-ba04-677c7c040988">MMDevice API</a>
 

 

