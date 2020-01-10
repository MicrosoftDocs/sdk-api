---
UID: NN:bdatif.ITuneRequestInfo
title: ITuneRequestInfo (bdatif.h)
description: The ITuneRequestInfo interface is implemented on the BDA MPEG2 Transport Information Filter (TIF) and is used by the Network Provider.
old-location: mstv\itunerequestinfo.htm
tech.root: mstv
ms.assetid: e5cb1a15-29c4-4e0f-aed2-eafe12ea007a
ms.date: 12/05/2018
ms.keywords: ITuneRequestInfo, ITuneRequestInfo interface [Microsoft TV Technologies], ITuneRequestInfo interface [Microsoft TV Technologies],described, ITuneRequestInfoInterface, bdatif/ITuneRequestInfo, mstv.itunerequestinfo
f1_keywords:
- bdatif/ITuneRequestInfo
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Bdatif.h
api_name:
- ITuneRequestInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITuneRequestInfo interface


## -description



The <b>ITuneRequestInfo</b> interface is implemented on the BDA MPEG2 Transport Information Filter (TIF) and is used by the Network Provider. When the Network Provider receives a tune request, it is not guaranteed that all the necessary locator information will be present in the locator object associated with the tune request. If information is missing, the Network Provider uses this interface to instruct the TIF to fill in the locator data. Similarly, a tune request might not contain a complete list of all the components (substreams) available on the service at a given time. After the Network Provider has tuned to a service, it can ask the TIF to fill in the component information associated with the tune request. An application can then re-examine the tune request after it has been submitted, and compare it to the list of default preferred component types to determine whether to tune to a particular audio stream, or inform the user of any substreams that were not mentioned in the EPG data. For more information, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_defaultpreferredcomponenttypes">ITuningSpace::get_DefaultPreferredComponentTypes</a>.

If the TIF is not able to provide the locator data for the transport stream, it must provide the default locator for the tuning space associated with the tune request.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITuneRequestInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITuneRequestInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-itunerequestinfo-createcomponentlist">CreateComponentList</a>
</td>
<td align="left" width="63%">
Creates a new <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/components-object">Components</a> collection for the tune request, and fills it in with all network-specific data after the receiver has tuned to the service.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-itunerequestinfo-getcomponentdata">GetComponentData</a>
</td>
<td align="left" width="63%">
Fills in all network-specific component data for the existing <a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/components-object">Components</a> collection on the specified tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-itunerequestinfo-getlocatordata">GetLocatorData</a>
</td>
<td align="left" width="63%">
Provides channel/program locator information for the specified tune request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-itunerequestinfo-getnextlocator">GetNextLocator</a>
</td>
<td align="left" width="63%">
Creates a new tune request with locator information for the next transport stream on the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-itunerequestinfo-getnextprogram">GetNextProgram</a>
</td>
<td align="left" width="63%">
Creates a new tune request with channel/program locator information for the next service on the current transport stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-itunerequestinfo-getpreviouslocator">GetPreviousLocator</a>
</td>
<td align="left" width="63%">
Creates a new tune request with locator information for the previous transport stream on the network.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/bdatif/nf-bdatif-itunerequestinfo-getpreviousprogram">GetPreviousProgram</a>
</td>
<td align="left" width="63%">
Creates a new tune request with locator information for the previous service on the current transport stream.

</td>
</tr>
</table> 


## -remarks



To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuneRequestInfo)</code>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
 

 

