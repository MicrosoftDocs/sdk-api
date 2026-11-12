---
UID: NF:uiautomationcore.IUiaEndpointNotifier.RegisterEndpoint
tech.root: WinAuto
title: IUiaEndpointNotifier::RegisterEndpoint
ms.date: 11/12/2026
targetos: Windows
description: Registers a UI Automation endpoint and its connection callback.
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
 - IUiaEndpointNotifier::RegisterEndpoint
f1_keywords:
 - IUiaEndpointNotifier::RegisterEndpoint
 - uiautomationcore/IUiaEndpointNotifier::RegisterEndpoint
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterEndpoint
---

# IUiaEndpointNotifier::RegisterEndpoint method

## -description

Registers a UI Automation endpoint and its connection callback.

## -parameters

### -param endpointId [in]

Type: **GUID**

The unique, nonzero GUID that identifies the endpoint. Use the same ID in the host-side placeholder and host association.

### -param notifier [in]

Type: **[IUiaEndpointNotifierCallback](nn-uiautomationcore-iuiaendpointnotifiercallback.md)\***

The callback that responds when a UI Automation client needs to connect to the endpoint.

## -returns

Returns **S_OK** on success, or an **HRESULT** error code on failure.

## -remarks

Each [IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md) instance manages one endpoint. Create a separate instance for each endpoint, rather than registering multiple endpoints on the same instance.

UI Automation holds a reference to *notifier* until [UnregisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-unregisterendpoint.md) is called or the notifier is released. Retain the notifier instance while the endpoint is registered.

After registration, associate the endpoint with a host by using **RegisterEndpointHostAsHwnd**, **RegisterEndpointHostAsCoreWindow**, or **RegisterEndpointHostAsEndpointId**. Registration alone does not provide the host-side placeholder needed for tree navigation.

## -see-also

[IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md)

[IUiaEndpointNotifier::RegisterEndpointHostAsHwnd](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostashwnd.md)

[IUiaEndpointNotifierCallback::OnCreateAutomationConnection](nf-uiautomationcore-iuiaendpointnotifiercallback-oncreateautomationconnection.md)
