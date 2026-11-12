---
UID: NN:uiautomationcore.IUIAutomationProviderApi
tech.root: WinAuto
title: IUIAutomationProviderApi
ms.date: 11/12/2026
targetos: Windows
description: Provides entry points for returning a UI Automation endpoint provider and obtaining its host provider.
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
 - IUIAutomationProviderApi
f1_keywords:
 - IUIAutomationProviderApi
 - uiautomationcore/IUIAutomationProviderApi
dev_langs:
 - c++
helpviewer_keywords:
 - IUIAutomationProviderApi
---

# IUIAutomationProviderApi interface

## -description

Provides entry points for returning a UI Automation endpoint provider and obtaining its host provider.

## -inheritance

The **IUIAutomationProviderApi** interface inherits from [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown).

## -remarks

Obtain this interface by calling [CoCreateInstance](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) with the **UIAutomationProviderApi** coclass, **CLSCTX_INPROC_SERVER**, and **IID_IUIAutomationProviderApi**. The coclass and interface are declared in **uiautomationcore.h**.

Use [UiaReturnRawElementProviderForEndpoint](nf-uiautomationcore-iuiautomationproviderapi-uiareturnrawelementproviderforendpoint.md) to respond to an endpoint connection request. Use [UiaHostProviderFromEndpoint](nf-uiautomationcore-iuiautomationproviderapi-uiahostproviderfromendpoint.md) from the endpoint root provider's **get_HostRawElementProvider** implementation.

These are COM methods, not standalone DLL exports. They are the endpoint equivalents of [UiaReturnRawElementProvider](/windows/win32/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiareturnrawelementprovider) and [UiaHostProviderFromHwnd](/windows/win32/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiahostproviderfromhwnd).

The interface exposes existing functionality in the system **UIAutomationCore.dll**. See [IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md) for registration and runtime availability detection.

The **Reserved0** method is reserved for internal use and must not be called.

## -see-also

[IUiaEndpointNotifier](nn-uiautomationcore-iuiaendpointnotifier.md)

[IUiaEndpointNotifierCallback](nn-uiautomationcore-iuiaendpointnotifiercallback.md)

[IRawElementProviderSimple::get_HostRawElementProvider](nf-uiautomationcore-irawelementprovidersimple-get_hostrawelementprovider.md)
