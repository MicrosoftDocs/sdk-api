---
UID: NF:uiautomationcore.IUIAutomationProviderApi.UiaReturnRawElementProviderForEndpoint
tech.root: WinAuto
title: IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint
ms.date: 11/12/2026
targetos: Windows
description: Supplies an endpoint's root provider in response to a UI Automation connection request.
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
 - IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint
f1_keywords:
 - IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint
 - uiautomationcore/IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint
dev_langs:
 - c++
helpviewer_keywords:
 - UiaReturnRawElementProviderForEndpoint
---

# IUIAutomationProviderApi::UiaReturnRawElementProviderForEndpoint method

## -description

Supplies an endpoint's root provider in response to a UI Automation connection request.

## -parameters

### -param endpointId [in]

Type: **GUID**

The endpoint ID supplied to **OnCreateAutomationConnection**.

### -param wParam [in]

Type: **WPARAM**

The connection name supplied to **OnCreateAutomationConnection**, cast with `reinterpret_cast<WPARAM>(connectionName)`. A copy containing the same string is also valid. The string must remain valid until this method returns.

### -param lParam [in]

Type: **LPARAM**

Set this parameter to `static_cast<LPARAM>(UiaRootObjectId)`.

### -param provider [in]

Type: **[IRawElementProviderSimple](nn-uiautomationcore-irawelementprovidersimple.md)\***

The endpoint's root provider. It must also implement [IRawElementProviderFragmentRoot](nn-uiautomationcore-irawelementproviderfragmentroot.md). If any component element exposes a nonempty **ElementId**, the root must implement [IComponentElementFinder](nn-uiautomationcore-icomponentelementfinder.md).

### -param resultOut [out]

Type: **LRESULT\***

Receives the result of the provider response. This value is separate from the method's **HRESULT** return value.

## -returns

Returns an **HRESULT** indicating the result of processing the request. Returns **E_INVALIDARG** if *endpointId* is **GUID_NULL**.

Passing a **NULL** provider or an object ID other than **UiaRootObjectId** does not establish a connection, even if the method returns **S_OK**.

## -remarks

Call this method from, or in response to, [IUiaEndpointNotifierCallback::OnCreateAutomationConnection](nf-uiautomationcore-iuiaendpointnotifiercallback-oncreateautomationconnection.md), and complete the response before the callback returns.

Unlike the window-based **UiaReturnRawElementProvider** function, this method takes an endpoint ID instead of an **HWND**, and *wParam* carries the connection name rather than a window message parameter.

The root provider's **get_HostRawElementProvider** implementation should call [UiaHostProviderFromEndpoint](nf-uiautomationcore-iuiautomationproviderapi-uiahostproviderfromendpoint.md) with the same endpoint ID.

### Example

The following helper responds to a callback after the application has obtained **IUIAutomationProviderApi** and its endpoint root provider. Call it on a thread where those interfaces can be used, and return its **HRESULT** from **OnCreateAutomationConnection**.

```cpp
HRESULT RespondToEndpointConnection(
    IUIAutomationProviderApi* providerApi,
    GUID endpointId,
    LPCWSTR connectionName,
    IRawElementProviderSimple* rootProvider)
{
    LRESULT result = 0;
    return providerApi->UiaReturnRawElementProviderForEndpoint(
        endpointId,
        reinterpret_cast<WPARAM>(connectionName),
        static_cast<LPARAM>(UiaRootObjectId),
        rootProvider,
        &result);
}
```

## -see-also

[IUIAutomationProviderApi](nn-uiautomationcore-iuiautomationproviderapi.md)

[IUiaEndpointNotifierCallback::OnCreateAutomationConnection](nf-uiautomationcore-iuiaendpointnotifiercallback-oncreateautomationconnection.md)

[UiaReturnRawElementProvider](/windows/win32/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiareturnrawelementprovider)
