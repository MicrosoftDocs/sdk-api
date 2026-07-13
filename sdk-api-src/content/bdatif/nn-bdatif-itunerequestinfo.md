---
UID: NN:bdatif.ITuneRequestInfo
title: ITuneRequestInfo (bdatif.h)
description: The ITuneRequestInfo interface is implemented on the BDA MPEG2 Transport Information Filter (TIF) and is used by the Network Provider.
helpviewer_keywords: ["ITuneRequestInfo","ITuneRequestInfo interface [Microsoft TV Technologies]","ITuneRequestInfo interface [Microsoft TV Technologies]","described","ITuneRequestInfoInterface","bdatif/ITuneRequestInfo","mstv.itunerequestinfo"]
old-location: mstv\itunerequestinfo.htm
tech.root: mstv
ms.assetid: e5cb1a15-29c4-4e0f-aed2-eafe12ea007a
ms.date: 12/05/2018
ms.keywords: ITuneRequestInfo, ITuneRequestInfo interface [Microsoft TV Technologies], ITuneRequestInfo interface [Microsoft TV Technologies],described, ITuneRequestInfoInterface, bdatif/ITuneRequestInfo, mstv.itunerequestinfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITuneRequestInfo
 - bdatif/ITuneRequestInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bdatif.h
api_name:
 - ITuneRequestInfo
---

# ITuneRequestInfo interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>ITuneRequestInfo</b> interface is implemented on the BDA MPEG2 Transport Information Filter (TIF) and is used by the Network Provider. When the Network Provider receives a tune request, it is not guaranteed that all the necessary locator information will be present in the locator object associated with the tune request. If information is missing, the Network Provider uses this interface to instruct the TIF to fill in the locator data. Similarly, a tune request might not contain a complete list of all the components (substreams) available on the service at a given time. After the Network Provider has tuned to a service, it can ask the TIF to fill in the component information associated with the tune request. An application can then re-examine the tune request after it has been submitted, and compare it to the list of default preferred component types to determine whether to tune to a particular audio stream, or inform the user of any substreams that were not mentioned in the EPG data. For more information, see <a href="/previous-versions/windows/desktop/api/tuner/nf-tuner-ituningspace-get_defaultpreferredcomponenttypes">ITuningSpace::get_DefaultPreferredComponentTypes</a>.

If the TIF is not able to provide the locator data for the transport stream, it must provide the default locator for the tuning space associated with the tune request.

## -inheritance

The <b>ITuneRequestInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITuneRequestInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(ITuneRequestInfo)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
