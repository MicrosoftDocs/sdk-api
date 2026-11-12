---
UID: NF:uiautomationcore.IUiaEndpointNotifierCallback.OnCreateAutomationConnection
tech.root: WinAuto
title: IUiaEndpointNotifierCallback::OnCreateAutomationConnection
ms.date: 11/12/2026
targetos: Windows
description: Requests the root provider for a connection to a UI Automation endpoint.
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
 - IUiaEndpointNotifierCallback::OnCreateAutomationConnection
f1_keywords:
 - IUiaEndpointNotifierCallback::OnCreateAutomationConnection
 - uiautomationcore/IUiaEndpointNotifierCallback::OnCreateAutomationConnection
dev_langs:
 - c++
helpviewer_keywords:
 - OnCreateAutomationConnection
---

# IUiaEndpointNotifierCallback::OnCreateAutomationConnection method

## -description

Requests the root provider for a connection to a UI Automation endpoint.

## -parameters

### -param endpointId [in]

Type: **GUID**

The ID of the registered endpoint to which the client is connecting.

### -param connectionName [in]

Type: **LPCWSTR**

A null-terminated string identifying the connection request. UI Automation owns this string, and it is valid only for the duration of this call. Do not free it or retain the pointer after returning.

## -returns

Return **S_OK** on success, or an **HRESULT** error code if the connection response fails.

## -remarks

Implement this method on the callback passed to [IUiaEndpointNotifier::RegisterEndpoint](nf-uiautomationcore-iuiaendpointnotifier-registerendpoint.md).

Respond by calling [IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint](nf-uiautomationcore-iuiautomationproviderapi-uiareturnrawelementproviderforendpoint.md) with *endpointId*, the endpoint's root provider, `reinterpret_cast<WPARAM>(connectionName)` as *wParam*, and `static_cast<LPARAM>(UiaRootObjectId)` as *lParam*. Return the **HRESULT** from the response.

The callback can run on an arbitrary UI Automation worker thread. If the provider requires another thread, dispatch the response in accordance with the provider's COM threading requirements and complete it before returning from this callback.

The connection name is matched by string content, not pointer identity. You can copy it when dispatching the response, but the string passed to **UiaReturnRawElementProviderForEndpoint** must remain valid until that call completes.

## -see-also

[IUiaEndpointNotifierCallback](nn-uiautomationcore-iuiaendpointnotifiercallback.md)

[IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint](nf-uiautomationcore-iuiautomationproviderapi-uiareturnrawelementproviderforendpoint.md)
