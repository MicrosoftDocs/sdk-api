---
UID: NF:uiautomationcore.IUIAutomationProviderApi.UiaHostProviderFromEndpoint
tech.root: WinAuto
title: IUIAutomationProviderApi::UiaHostProviderFromEndpoint
ms.date: 11/12/2026
targetos: Windows
description: Retrieves the host provider for a UI Automation endpoint.
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
 - IUIAutomationProviderApi::UiaHostProviderFromEndpoint
f1_keywords:
 - IUIAutomationProviderApi::UiaHostProviderFromEndpoint
 - uiautomationcore/IUIAutomationProviderApi::UiaHostProviderFromEndpoint
dev_langs:
 - c++
helpviewer_keywords:
 - UiaHostProviderFromEndpoint
---

# IUIAutomationProviderApi::UiaHostProviderFromEndpoint method

## -description

Retrieves the host provider for a UI Automation endpoint.

## -parameters

### -param endpointId [in]

Type: **GUID**

The nonzero GUID identifying the endpoint.

### -param hostProviderOut [out]

Type: **[IRawElementProviderSimple](nn-uiautomationcore-irawelementprovidersimple.md)\*\***

Receives the host provider. Release the returned interface pointer when it is no longer needed, unless ownership is being transferred to the caller of **get_HostRawElementProvider**.

## -returns

Returns **S_OK** on success, or an **HRESULT** error code on failure.

Returns **E_INVALIDARG** if *endpointId* is **GUID_NULL** or *hostProviderOut* is **NULL**.

## -remarks

In the endpoint root provider's [IRawElementProviderSimple::get_HostRawElementProvider](nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider.md) implementation, call this method with the endpoint ID and pass the output back to UI Automation.

This is the endpoint equivalent of **UiaHostProviderFromHwnd**. It enables UI Automation to connect the endpoint's provider tree to its registered host.

## -see-also

[IUIAutomationProviderApi](nn-uiautomationcore-iuiautomationproviderapi.md)

[UiaHostProviderFromHwnd](/windows/win32/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiahostproviderfromhwnd)

[IRawElementProviderComponentHostRoot](nn-uiautomationcore-irawelementprovidercomponenthostroot.md)
