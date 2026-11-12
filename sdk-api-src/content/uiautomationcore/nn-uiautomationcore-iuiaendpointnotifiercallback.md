---
UID: NN:uiautomationcore.IUiaEndpointNotifierCallback
tech.root: WinAuto
title: IUiaEndpointNotifierCallback
ms.date: 11/12/2026
targetos: Windows
description: Receives requests to connect a UI Automation client to an endpoint provider.
prerelease: false
req.construct-type: iface
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
 - IUiaEndpointNotifierCallback
f1_keywords:
 - IUiaEndpointNotifierCallback
 - uiautomationcore/IUiaEndpointNotifierCallback
dev_langs:
 - c++
helpviewer_keywords:
 - IUiaEndpointNotifierCallback
---

# IUiaEndpointNotifierCallback interface

## -description

Receives requests to connect a UI Automation client to an endpoint provider.

## -inheritance

The **IUiaEndpointNotifierCallback** interface inherits from [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

## -remarks

Endpoint providers implement this interface and pass it to [IUiaEndpointNotifier::RegisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-registerendpoint.md). UI Automation holds a reference to the callback until the endpoint is unregistered or the notifier is released.

UI Automation calls [OnCreateAutomationConnection](nf-uiautomationcore-iuiaendpointnotifiercallback-oncreateautomationconnection.md) when a client needs to connect to the endpoint. Respond with the endpoint's root provider through [IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint](nf-uiautomationcore-iuiautomationproviderapi-uiareturnrawelementproviderforendpoint.md).

The callback can be invoked on an arbitrary UI Automation worker thread, not necessarily the thread that registered the endpoint. Complete the provider response before returning from the callback.

## -see-also

[IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md)

[IUIAutomationProviderApi](nn-uiautomationcore-iuiautomationproviderapi.md)
