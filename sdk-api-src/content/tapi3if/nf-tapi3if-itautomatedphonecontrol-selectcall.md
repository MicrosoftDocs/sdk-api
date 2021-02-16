---
UID: NF:tapi3if.ITAutomatedPhoneControl.SelectCall
title: ITAutomatedPhoneControl::SelectCall (tapi3if.h)
description: The SelectCall method selects the current phone object onto the Call object pointed to by the pCall parameter.
helpviewer_keywords: ["ITAutomatedPhoneControl interface [TAPI 2.2]","SelectCall method","ITAutomatedPhoneControl.SelectCall","ITAutomatedPhoneControl::SelectCall","SelectCall","SelectCall method [TAPI 2.2]","SelectCall method [TAPI 2.2]","ITAutomatedPhoneControl interface","_tapi3_itautomatedphonecontrol_selectcall","tapi3.itautomatedphonecontrol_selectcall","tapi3if/ITAutomatedPhoneControl::SelectCall"]
old-location: tapi3\itautomatedphonecontrol_selectcall.htm
tech.root: tapi3
ms.assetid: b9e721cb-8f62-420d-bfc1-f8e634f0f2d4
ms.date: 12/05/2018
ms.keywords: ITAutomatedPhoneControl interface [TAPI 2.2],SelectCall method, ITAutomatedPhoneControl.SelectCall, ITAutomatedPhoneControl::SelectCall, SelectCall, SelectCall method [TAPI 2.2], SelectCall method [TAPI 2.2],ITAutomatedPhoneControl interface, _tapi3_itautomatedphonecontrol_selectcall, tapi3.itautomatedphonecontrol_selectcall, tapi3if/ITAutomatedPhoneControl::SelectCall
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
 - ITAutomatedPhoneControl::SelectCall
 - tapi3if/ITAutomatedPhoneControl::SelectCall
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
 - ITAutomatedPhoneControl.SelectCall
---

# ITAutomatedPhoneControl::SelectCall


## -description

The 
<b>SelectCall</b> method selects the current phone object onto the Call object pointed to by the <i>pCall</i> parameter.

## -parameters

### -param pCall [in]

Pointer to the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface.

### -param fSelectDefaultTerminals [in]

If VARIANT_TRUE, use default terminals. For more information, see the following Remarks section.

## -returns

If the method succeeds, it returns S_OK. Otherwise, it returns an error value.

## -remarks

The application must have owner privilege on both the call and the phone for this method to return success. If the phone is not already open with owner privilege, this method fails.

If the <i>fSelectDefaultTerminals</i> parameter is set to VARIANT_TRUE, this method retrieves all the default terminals associated with the phone and attempts to select them on the call. If instantiation of one of the terminals fails, or if selection of one of the terminals on the call fails, then the entire 
<b>SelectCall</b> method will return failure, and the call will not be selected on the phone. If this is not the required behavior for an application, then the application should pass in VARIANT_FALSE for the <i>fSelectDefaultTerminals</i> parameter and handle terminal selection separately.

On successful completion of this method, the phone object keeps a reference to the call object (that is, it calls the 
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-addref">AddRef</a> method on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>).

For Windows XP, only one call at a time can be selected on a phone. Future versions of TAPI may support simultaneous selection of multiple calls for use with phones that support multiple call appearances.

Note that a call can be unselected in two ways: (1) the application can invoke 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-unselectcall">ITAutomatedPhoneControl::UnselectCall</a>, or (2) the phone object itself can invoke <b>ITAutomatedPhoneControl::UnselectCall</b>. See the following list for information on when this happens.

After this method completes successfully, the following handling is performed on the selected call:

<ul>
<li>When the phone goes onhook, the phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-disconnect">ITBasicCallControl::Disconnect</a> on any currently handled call that is not already in the CS_DISCONNECTED call state.</li>
<li>If a selected call reaches the CS_DISCONNECTED call state, then the phone object automatically unselects the call using the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-unselectcall">ITAutomatedPhoneControl::UnselectCall</a> method.</li>
<li>If the phone is closed, any selected call is automatically unselected from that phone.</li>
<li>When the phone goes offhook, or a call is selected when the phone is offhook, the phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer">ITBasicCallControl::Answer</a> on the currently handled call if it is in the CS_OFFERING call state.</li>
<li>The phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-starttone">ITAutomatedPhoneControl::StartTone</a>( PT_RINGBACK, 0 ) on itself when a call is selected on it in the CS_INPROGRESS call state and the phone is offhook, or when a call that has been selected on the phone enters the CS_INPROGRESS call state and the phone is offhook.</li>
<li>The phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stoptone">ITAutomatedPhoneControl::StopTone</a> on itself when a call is selected on it in the CS_CONNECTED call state, or when a call that has been selected on the phone enters the CS_CONNECTED call state.</li>
<li>The phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-startringer">ITAutomatedPhoneControl::StartRinger</a>( 0, 0 ) on itself when a call is selected on it in the CS_OFFERING, CS_INPROGRESS, or CS_CONNECTED call state and the phone is onhook. This also occurs when a call that has been selected on the phone enters the CS_OFFERING, CS_INPROGRESS, or CS_CONNECTED call state and the phone is onhook.</li>
</ul>
Depending on the circumstances, the phone object performs one of the following actions when a call is selected on it in the CS_DISCONNECTED call state, or when a call that has been selected on the phone enters the CS_DISCONNECTED call state.

<ul>
<li>If the phone is onhook, then the phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stopringer">ITAutomatedPhoneControl::StopRinger</a> on itself.</li>
<li>If the phone is offhook and the CS_DISCONNECTED call state event has cause equal to CEC_DISCONNECT_BUSY, then the phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-starttone">ITAutomatedPhoneControl::StartTone</a>( PT_BUSY, 0 ).</li>
<li>If the phone is offhook and the CS_DISCONNECTED call state event has cause equal to CEC_DISCONNECT_NORMAL, then the phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-stoptone">ITAutomatedPhoneControl::StopTone</a>.</li>
<li>If the phone is offhook and the CS_DISCONNECTED call state event has neither cause CEC_DISCONNECT_BUSY nor cause CEC_DISCONNECT_NORMAL, then the phone object calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itautomatedphonecontrol-starttone">ITAutomatedPhoneControl::StartTone</a>( PT_ERROR, 0 ).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itautomatedphonecontrol">ITAutomatedPhoneControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>