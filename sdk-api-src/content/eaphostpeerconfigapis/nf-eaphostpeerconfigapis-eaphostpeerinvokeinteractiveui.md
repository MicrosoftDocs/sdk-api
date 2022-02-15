---
UID: NF:eaphostpeerconfigapis.EapHostPeerInvokeInteractiveUI
title: EapHostPeerInvokeInteractiveUI function (eaphostpeerconfigapis.h)
description: Raises an interactive user interface used to get credentials from the user.
helpviewer_keywords: ["EapHostPeerInvokeInteractiveUI","EapHostPeerInvokeInteractiveUI function [EAPHost]","eaphost.eaphostpeerinvokeinteractiveui","eaphostpeerconfigapis/EapHostPeerInvokeInteractiveUI"]
old-location: eaphost\eaphostpeerinvokeinteractiveui.htm
tech.root: eaphost
ms.assetid: a4a46b77-f8ab-4062-b966-1590ea9e46d2
ms.date: 12/05/2018
ms.keywords: EapHostPeerInvokeInteractiveUI, EapHostPeerInvokeInteractiveUI function [EAPHost], eaphost.eaphostpeerinvokeinteractiveui, eaphostpeerconfigapis/EapHostPeerInvokeInteractiveUI
req.header: eaphostpeerconfigapis.h
req.include-header: 
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
req.lib: Eappcfg.lib
req.dll: Eappcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - EapHostPeerInvokeInteractiveUI
 - eaphostpeerconfigapis/EapHostPeerInvokeInteractiveUI
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - eappcfg.dll
api_name:
 - EapHostPeerInvokeInteractiveUI
---

# EapHostPeerInvokeInteractiveUI function


## -description

Raises an interactive user interface used to get credentials from the user. For example, this function can be used to raise a UI that retrieves credentials from a smart card, and prompts the user to enter the corresponding PIN.

<b>EapHostPeerInvokeInteractiveUI</b> must be called on threads that have COM initialized for <a href="/previous-versions/ms810413(v=msdn.10)">Single Threaded Apartment</a>. This can be achieved by calling COM API <a href="/windows/desktop/api/objbase/nf-objbase-coinitialize">CoInitialize</a>; when the supplicant has finished  with the STA thread <a href="/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize">CoUninitialize</a> must be called before exiting.

## -parameters

### -param hwndParent [in]

The handle of the parent window under which configuration dialog appears.

### -param dwSizeofUIContextData [in]

The size, in bytes, of the buffer pointed to by the <i>pUIContextData</i> parameter.

### -param pUIContextData [in]

A pointer to a buffer that contains the supplicant UI context data from EAPHost. The context data is returned by  <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext">EapHostPeerGetUIContext</a>. The buffer  is of size <i>dwSizeOfUIContextData</i>.

### -param pdwSizeOfDataFromInteractiveUI [out]

A pointer to a DWORD  that represents the size, in bytes, of the buffer pointed to by the <i>ppDataFromInteractiveUI</i> parameter.

### -param ppDataFromInteractiveUI [out]

A pointer to a pointer to a byte buffer that  contains data from the interactive UI necessary for authentication to continue. The parameter <i>ppDataFromInteractiveUI</i> should be passed to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext">EapHostPeerSetUIContext</a> as the IN parameter <i>pUIContextData</i>. After consuming the data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreememory">EapHostPeerFreeMemory</a>. The buffer is of size <i>pdwSizeofDataFromInteractiveUI</i>.

### -param ppEapError [out]

A pointer to a pointer to an <a href="/windows/desktop/api/eaptypes/ns-eaptypes-eap_error">EAP_ERROR</a> structure that contains any errors raised by EAPHost during  the execution of this function call. After consuming the error data, this memory must be freed by calling <a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerfreeerrormemory">EapHostPeerFreeErrorMemory</a>.

## -remarks

The supplicant should call [EAP_E_EAPHOST_METHOD_OPERATION_NOT_SUPPORTED](/windows/win32/eaphost/eap-related-error-and-information-constants) is returned, the supplicant should resort to the traditional model of invoking method interactive UI by calling <b>EapHostPeerInvokeInteractiveUI</b>. 

If called,<b>EapHostPeerInvokeInteractiveUI</b> raises the user interface for the EAP method after the supplicant calls <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext">EapHostPeerGetUIContext</a>. This occurs when a call to <a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerprocessreceivedpacket">EapHostPeerProcessReceivedPacket</a> 
   returns the <b>EapHostPeerResponseInvokeUi</b> action code. <b>EapHostPeerGetUIContext</b> returns UI context that 
   the supplicant then passes to <b>EapHostPeerInvokeInteractiveUI</b> to raise the UI.

## -see-also

[EAPHost Supplicant Configuration Functions](/windows/win32/eaphost/eap-host-supplicant-configuration-functions)



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeergetuicontext">EapHostPeerGetUIContext</a>



<a href="/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerqueryinteractiveuiinputfields">EapHostPeerQueryInteractiveUIInputFields</a>



<a href="/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeersetuicontext">EapHostPeerSetUIContext</a>