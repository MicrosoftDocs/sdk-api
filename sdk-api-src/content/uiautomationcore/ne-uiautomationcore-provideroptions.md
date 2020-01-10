---
UID: NE:uiautomationcore.ProviderOptions
title: ProviderOptions (uiautomationcore.h)
description: Contains values that specify the type of UI Automation provider. The IRawElementProviderSimple::ProviderOptions property uses this enumeration.
old-location: winauto\uiauto_ProvOptionsEnum.htm
tech.root: WinAuto
ms.assetid: ed13b168-f0c2-49d8-b613-2c62a6e060bd
ms.date: 12/05/2018
ms.keywords: ProviderOptions, ProviderOptions enumeration [Windows Accessibility], ProviderOptions_ClientSideProvider, ProviderOptions_HasNativeIAccessible, ProviderOptions_NonClientAreaProvider, ProviderOptions_OverrideProvider, ProviderOptions_ProviderOwnsSetFocus, ProviderOptions_RefuseNonClientSupport, ProviderOptions_ServerSideProvider, ProviderOptions_UseClientCoordinates, ProviderOptions_UseComThreading, uiauto.uiauto_ProvOptionsEnum, uiauto_ProvOptionsEnum, uiautomationcore/ProviderOptions, uiautomationcore/ProviderOptions_ClientSideProvider, uiautomationcore/ProviderOptions_HasNativeIAccessible, uiautomationcore/ProviderOptions_NonClientAreaProvider, uiautomationcore/ProviderOptions_OverrideProvider, uiautomationcore/ProviderOptions_ProviderOwnsSetFocus, uiautomationcore/ProviderOptions_RefuseNonClientSupport, uiautomationcore/ProviderOptions_ServerSideProvider, uiautomationcore/ProviderOptions_UseClientCoordinates, uiautomationcore/ProviderOptions_UseComThreading, winauto.uiauto_ProvOptionsEnum
f1_keywords:
- uiautomationcore/ProviderOptions
dev_langs:
- c++
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- UIAutomationCore.h
api_name:
- ProviderOptions
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ProviderOptions enumeration


## -description


Contains values that specify the type of UI Automation provider. The <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovidersimple-get_provideroptions">IRawElementProviderSimple::ProviderOptions</a> property uses this enumeration.


## -enum-fields




### -field ProviderOptions_ClientSideProvider

The provider is a client-side (proxy) provider.


### -field ProviderOptions_ServerSideProvider

The provider is a server-side provider.


### -field ProviderOptions_NonClientAreaProvider

The provider is a non-client-area provider.  


### -field ProviderOptions_OverrideProvider

The provider overrides another provider.


### -field ProviderOptions_ProviderOwnsSetFocus

The provider handles its own focus, and does not want UI Automation to set focus to the nearest window on its behalf. This option is typically used by providers for windows that appear to take focus without actually receiving Win32 focus, such as menus and drop-downs. 


### -field ProviderOptions_UseComThreading

The provider has explicit support for COM threading models, so that calls by UI Automation on COM-based providers are received on the appropriate thread. This means that STA-based provider implementations will be called back on their own STA thread, and therefore do not need extra synchronization to safely access resources that belong to that STA. MTA-based provider implementations will be called back on some other thread in the MTA, and will require appropriate synchronization to be added, as is usual for MTA code.


### -field ProviderOptions_RefuseNonClientSupport

The provider handles its own non-client area and does not want UI Automation to provide default accessibility support for controls in the non-client area, such as minimize/maximize buttons and menu bars.


### -field ProviderOptions_HasNativeIAccessible

The provider implements the <a href="https://docs.microsoft.com/windows/desktop/api/oleacc/nn-oleacc-iaccessible">IAccessible</a> interface. 


### -field ProviderOptions_UseClientCoordinates

The provider works in client coordinates instead of screen coordinates.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementproviderfragment-setfocus">SetFocus</a>
 

 

