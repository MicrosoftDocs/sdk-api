---
UID: NN:tapi3if.ITAutomatedPhoneControl
title: ITAutomatedPhoneControl (tapi3if.h)
description: The ITAutomatedPhoneControl is a fully OLE automatable and scriptable interface exposed by the TAPI phone object.
helpviewer_keywords: ["ITAutomatedPhoneControl","ITAutomatedPhoneControl interface [TAPI 2.2]","ITAutomatedPhoneControl interface [TAPI 2.2]","described","_tapi3_itautomatedphonecontrol","tapi3.itautomatedphonecontrol","tapi3if/ITAutomatedPhoneControl"]
old-location: tapi3\itautomatedphonecontrol.htm
tech.root: tapi3
ms.assetid: 60d4f079-75ee-4aeb-9e7c-0b16d90da754
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl, ITAutomatedPhoneControl interface [TAPI 2.2], ITAutomatedPhoneControl interface [TAPI 2.2],described, _tapi3_itautomatedphonecontrol, tapi3.itautomatedphonecontrol, tapi3if/ITAutomatedPhoneControl
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITAutomatedPhoneControl
 - tapi3if/ITAutomatedPhoneControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAutomatedPhoneControl
---

# ITAutomatedPhoneControl interface


## -description

The 
<b>ITAutomatedPhoneControl</b> is a fully OLE automatable and scriptable interface exposed by the TAPI phone object. When a phone device is opened with owner privilege, you can call the 
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a> interface to obtain an 
<b>ITAutomatedPhoneControl</b> interface pointer.

This interface performs several high-level phone-related functions:
<ul>
<li>Enable and configure automated control of the phone's tones and rings based on input from the phone's hookswitch and buttons.</li>
<li>Enable and configure automated call handling based on the phone's hookswitch state. For example, when the phone goes onhook while it is handling a connected call, the phone object can automatically invoke 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">ITBasicCallControl::Disconnect</a> on that call.</li>
<li>Generate specific tones on the audio devices associated with the phone, without accessing any audio APIs directly. The tone control allows an application to play tones on the audio devices associated with the phone, outside of the context of a call. Because these tones are not transmitted on any call, they are independent of the audio streaming functionality accessed through terminals.</li>
<li>Ring the phone without requiring information on whether the phone has a ringer and, if the phone has a ringer, determine the types of rings the phone supports.</li>
</ul>

## -inheritance

The <b>ITAutomatedPhoneControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITAutomatedPhoneControl</b> also has these types of members:

## -remarks

An 
<b>ITAutomatedPhoneControl</b> pointer becomes invalid when the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itphone-close">ITPhone::Close</a> method is called.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itphone">ITPhone</a>
