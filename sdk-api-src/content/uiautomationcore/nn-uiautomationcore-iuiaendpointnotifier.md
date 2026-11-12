---
UID: NN:uiautomationcore.IUiaEndpointNotifier
tech.root: WinAuto
title: IUiaEndpointNotifier
ms.date: 11/12/2026
targetos: Windows
description: Registers and manages a UI Automation endpoint whose provider can run in a different process from its host window.
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
 - IUiaEndpointNotifier
f1_keywords:
 - IUiaEndpointNotifier
 - uiautomationcore/IUiaEndpointNotifier
dev_langs:
 - c++
helpviewer_keywords:
 - IUiaEndpointNotifier
---

# IUiaEndpointNotifier interface

## -description

Registers and manages a UI Automation endpoint whose provider can run in a different process from its host window.

## -inheritance

The **IUiaEndpointNotifier** interface inherits from [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

## -remarks

A UI Automation endpoint exposes a provider tree that is integrated into the UI Automation tree of a host window or another endpoint. The provider does not need to own the host window. UI Automation clients navigate the combined tree without using the endpoint registration interfaces themselves.

An endpoint is identified by a GUID shared between the host and provider. Generate a unique, nonzero endpoint ID, for example by calling [CoCreateGuid](/windows/win32/api/combaseapi/nf-combaseapi-cocreateguid). The host and provider must exchange this ID; these APIs do not discover endpoints for the application.

To obtain this interface, call [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with **CLSID_UiaEndpointNotifier**, **CLSCTX_INPROC_SERVER**, and **IID_IUiaEndpointNotifier**. **CLSID_UiaEndpointNotifier** is declared in **uiautomationcoreapi.h**.

Use a Windows SDK that declares the endpoint interfaces. Successful creation of the endpoint notifier indicates that endpoint support is present on the running system. These declarations expose existing COM functionality; they do not require an application to deploy a replacement **UIAutomationCore.dll**.

Each notifier instance manages one endpoint. Create a separate notifier instance for each endpoint, and retain it for the lifetime of the registration.

### Registering an endpoint

1. Implement [IUiaEndpointNotifierCallback](nn-uiautomationcore-iuiaendpointnotifiercallback.md).
2. Call [RegisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-registerendpoint.md) with the endpoint ID and callback.
3. Associate the endpoint with its host by calling [RegisterEndpointHostAsHwnd](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostashwnd.md), [RegisterEndpointHostAsCoreWindow](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostascorewindow.md), or [RegisterEndpointHostAsEndpointId](nf-uiautomationcore-iuiaendpointnotifier-registerendpointhostasendpointid.md).
4. Expose a host-side placeholder implementing [IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md). Its **ComponentSiteId** identifies the endpoint to connect to.
5. When UI Automation calls **OnCreateAutomationConnection**, respond with the endpoint's root provider through [IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint](nf-uiautomationcore-iuiautomationproviderapi-uiareturnrawelementproviderforendpoint.md).
6. Call [UnregisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-unregisterendpoint.md) before shutting down the endpoint.

Implement [IRawElementProviderComponentHostRoot](nn-uiautomationcore-irawelementprovidercomponenthostroot.md) on the host's root provider to resolve navigation back to the host-side parent.

The callback can be invoked on an arbitrary UI Automation worker thread. If the provider must respond on another thread, marshal access to the provider as required by its COM threading model and wait for the response to complete before returning from the callback.

## -see-also

[IUiaEndpointNotifierCallback](nn-uiautomationcore-iuiaendpointnotifiercallback.md)

[IUIAutomationProviderApi](nn-uiautomationcore-iuiautomationproviderapi.md)

[IRawElementProviderComponent](nn-uiautomationcore-irawelementprovidercomponent.md)
