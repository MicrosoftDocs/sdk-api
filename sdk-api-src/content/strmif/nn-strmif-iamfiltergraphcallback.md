---
UID: NN:strmif.IAMFilterGraphCallback
title: IAMFilterGraphCallback (strmif.h)
author: windows-sdk-content
description: The IAMFilterGraphCallback interface provides a callback mechanism during graph building.To use this interface, implement the interface in your application or client object.
old-location: dshow\iamfiltergraphcallback.htm
tech.root: DirectShow
ms.assetid: 064acc6a-ba2f-4394-a3bf-a9b70e30e07e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAMFilterGraphCallback, IAMFilterGraphCallback interface [DirectShow], IAMFilterGraphCallback interface [DirectShow],described, IAMFilterGraphCallbackInterface, dshow.iamfiltergraphcallback, strmif/IAMFilterGraphCallback
ms.topic: interface
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - IAMFilterGraphCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMFilterGraphCallback interface


## -description



The <code>IAMFilterGraphCallback</code> interface provides a callback mechanism during graph building.

To use this interface, implement the interface in your application or client object. Query the Filter Graph Manager for the <b>IObjectWithSite</b> interface and call the <b>IObjectWithSite::SetSite</b> method with a pointer to your implementation of the interface. During graph building, if the Filter Graph Manager fails to render a pin, it calls the <b>UnabletoRender</b> method. The client can then take appropriate action, such as providing an error message for the user or registering a new filter.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IAMFilterGraphCallback</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IAMFilterGraphCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IAMFilterGraphCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c7fa0eae-f950-423a-8a89-9a7619b27ce6">UnableToRender</a>
</td>
<td align="left" width="63%">
Informs the client that no combination of filters could be found to render the specified pin.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/4d8e45e3-7144-44ad-b79e-5acc0cec6ed4">IAMGraphBuilderCallback Interface</a>
 

 

