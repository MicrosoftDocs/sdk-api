---
UID: NF:uiautomationcore.IProxyProviderWinEventSink.AddAutomationPropertyChangedEvent
title: IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent (uiautomationcore.h)
description: Raises a property-changed event.
helpviewer_keywords: ["AddAutomationPropertyChangedEvent","AddAutomationPropertyChangedEvent method [Windows Accessibility]","AddAutomationPropertyChangedEvent method [Windows Accessibility]","IProxyProviderWinEventSink interface","IProxyProviderWinEventSink interface [Windows Accessibility]","AddAutomationPropertyChangedEvent method","IProxyProviderWinEventSink.AddAutomationPropertyChangedEvent","IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent","uiauto.uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent","uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent","uiautomationcore/IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent","winauto.uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent"]
old-location: winauto\uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent.htm
tech.root: WinAuto
ms.assetid: 84b8db1d-75ec-45b6-a4a5-c5d4bffe6978
ms.date: 12/05/2018
ms.keywords: AddAutomationPropertyChangedEvent, AddAutomationPropertyChangedEvent method [Windows Accessibility], AddAutomationPropertyChangedEvent method [Windows Accessibility],IProxyProviderWinEventSink interface, IProxyProviderWinEventSink interface [Windows Accessibility],AddAutomationPropertyChangedEvent method, IProxyProviderWinEventSink.AddAutomationPropertyChangedEvent, IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent, uiauto.uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent, uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent, uiautomationcore/IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent, winauto.uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent
 - uiautomationcore/IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IProxyProviderWinEventSink.AddAutomationPropertyChangedEvent
---

# IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent


## -description

Raises a property-changed event.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

A pointer to the provider for the element that will raise the event.

### -param id [in]

Type: <b>PROPERTYID</b>

The identifier of the property that is to be changed. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param newValue [in]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a></b>

The new value for the changed property.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iproxyproviderwineventsink">IProxyProviderWinEventSink</a>