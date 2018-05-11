---
UID: NN:bdatif.ITuneRequestInfo
title: ITuneRequestInfo
author: windows-driver-content
description: The ITuneRequestInfo interface is implemented on the BDA MPEG2 Transport Information Filter (TIF) and is used by the Network Provider.
old-location: mstv\itunerequestinfo.htm
old-project: mstv
ms.assetid: e5cb1a15-29c4-4e0f-aed2-eafe12ea007a
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITuneRequestInfo, ITuneRequestInfo interface [Microsoft TV Technologies], ITuneRequestInfo interface [Microsoft TV Technologies],described, ITuneRequestInfoInterface, bdatif/ITuneRequestInfo, mstv.itunerequestinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: bdatif.h
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
req.typenames: SmartCardApplication
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Bdatif.h
api_name:
-	ITuneRequestInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ITuneRequestInfo interface


## -description



The <b>ITuneRequestInfo</b> interface is implemented on the BDA MPEG2 Transport Information Filter (TIF) and is used by the Network Provider. When the Network Provider receives a tune request, it is not guaranteed that all the necessary locator information will be present in the locator object associated with the tune request. If information is missing, the Network Provider uses this interface to instruct the TIF to fill in the locator data. Similarly, a tune request might not contain a complete list of all the components (substreams) available on the service at a given time. After the Network Provider has tuned to a service, it can ask the TIF to fill in the component information associated with the tune request. An application can then re-examine the tune request after it has been submitted, and compare it to the list of default preferred component types to determine whether to tune to a particular audio stream, or inform the user of any substreams that were not mentioned in the EPG data. For more information, see <a href="https://msdn.microsoft.com/a633a94c-e514-46b1-9982-7526ffa89b74">ITuningSpace::get_DefaultPreferredComponentTypes</a>.

If the TIF is not able to provide the locator data for the transport stream, it must provide the default locator for the tuning space associated with the tune request.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuneRequestInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITuneRequestInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITuneRequestInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb4ec234-1e94-4c9f-8372-a5972df18948">CreateComponentList</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://msdn.microsoft.com/library/windows/hardware/dn922646">Components</a> collection for the tune request, and fills it in with all network-specific data after the receiver has tuned to the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/769d112e-4df7-451c-ac12-440b16c33e88">GetComponentData</a>
</td>
<td align="left" width="63%">
Fills in all network-specific component data for the existing <a href="https://msdn.microsoft.com/library/windows/hardware/dn922646">Components</a> collection on the specified tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c325d61d-c99b-4033-bd16-36b74fc38d07">GetLocatorData</a>
</td>
<td align="left" width="63%">
Provides channel/program locator information for the specified tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/300479bf-f8e3-41e2-898e-8a87e4abc801">GetNextLocator</a>
</td>
<td align="left" width="63%">
Creates a new tune request with locator information for the next transport stream on the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ed1c5a30-19fb-46a8-b521-017da56d85c8">GetNextProgram</a>
</td>
<td align="left" width="63%">
Creates a new tune request with channel/program locator information for the next service on the current transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72512da5-28d4-40b8-93df-039014f432c0">GetPreviousLocator</a>
</td>
<td align="left" width="63%">
Creates a new tune request with locator information for the previous transport stream on the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9c03a5c9-9dc1-4163-bbc8-8dae2037eb24">GetPreviousProgram</a>
</td>
<td align="left" width="63%">
Creates a new tune request with locator information for the previous service on the current transport stream.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuneRequestInfo)</code>.




## -see-also




<a href="https://msdn.microsoft.com/07d18f73-e852-4c88-a2e2-e8f4198ca799">BDA Interfaces</a>
 

 

