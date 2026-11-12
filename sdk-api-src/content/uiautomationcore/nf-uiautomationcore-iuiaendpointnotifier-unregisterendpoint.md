---
UID: NF:uiautomationcore.IUiaEndpointNotifier.UnregisterEndpoint
tech.root: WinAuto
title: IUiaEndpointNotifier::UnregisterEndpoint
ms.date: 11/12/2026
targetos: Windows
description: Unregisters the endpoint managed by this notifier.
prerelease: false
req.construct-type: function
req.header: uiautomationcore.h
req.idl: UIAutomationCore.idl
req.target-min-winverclnt:
req.target-min-winversvr:
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - uiautomationcore.h
api_name:
 - IUiaEndpointNotifier::UnregisterEndpoint
f1_keywords:
 - IUiaEndpointNotifier::UnregisterEndpoint
 - uiautomationcore/IUiaEndpointNotifier::UnregisterEndpoint
dev_langs:
 - c++
helpviewer_keywords:
 - UnregisterEndpoint
---

# IUiaEndpointNotifier::UnregisterEndpoint method

## -description

Unregisters the endpoint managed by this notifier.

## -returns

Returns **S_OK** on success, or an **HRESULT** error code on failure.

## -remarks

Call this method before shutting down the endpoint. Each [IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md) instance manages one registration, so no endpoint ID parameter is required.

Unregistration releases the registration and the notifier's reference to its callback. Releasing the notifier also unregisters its endpoint.

Unregistering prevents new connections from being routed to the registration. It does not forcibly disconnect existing clients or release provider references already held by those clients.

## -see-also

[IUiaEndpointNotifier::RegisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-registerendpoint.md)

[IUiaEndpointNotifierCallback](nn-uiautomationcore-iuiaendpointnotifiercallback.md)
