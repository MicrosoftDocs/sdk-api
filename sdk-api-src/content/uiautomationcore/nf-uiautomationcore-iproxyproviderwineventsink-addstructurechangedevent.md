---
UID: NF:uiautomationcore.IProxyProviderWinEventSink.AddStructureChangedEvent
title: IProxyProviderWinEventSink::AddStructureChangedEvent (uiautomationcore.h)
description: Raises an event to notify clients that the structure of the UI Automation tree has changed.
helpviewer_keywords: ["AddStructureChangedEvent","AddStructureChangedEvent method [Windows Accessibility]","AddStructureChangedEvent method [Windows Accessibility]","IProxyProviderWinEventSink interface","IProxyProviderWinEventSink interface [Windows Accessibility]","AddStructureChangedEvent method","IProxyProviderWinEventSink.AddStructureChangedEvent","IProxyProviderWinEventSink::AddStructureChangedEvent","uiauto.uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent","uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent","uiautomationcore/IProxyProviderWinEventSink::AddStructureChangedEvent","winauto.uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent"]
old-location: winauto\uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent.htm
tech.root: WinAuto
ms.assetid: 03be09a6-da4d-4071-bd7c-df79688c20d3
ms.date: 12/05/2018
ms.keywords: AddStructureChangedEvent, AddStructureChangedEvent method [Windows Accessibility], AddStructureChangedEvent method [Windows Accessibility],IProxyProviderWinEventSink interface, IProxyProviderWinEventSink interface [Windows Accessibility],AddStructureChangedEvent method, IProxyProviderWinEventSink.AddStructureChangedEvent, IProxyProviderWinEventSink::AddStructureChangedEvent, uiauto.uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent, uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent, uiautomationcore/IProxyProviderWinEventSink::AddStructureChangedEvent, winauto.uiauto_IProxyProviderWinEventSink_AddStructureChangedEvent
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
 - IProxyProviderWinEventSink::AddStructureChangedEvent
 - uiautomationcore/IProxyProviderWinEventSink::AddStructureChangedEvent
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
 - IProxyProviderWinEventSink.AddStructureChangedEvent
---

# IProxyProviderWinEventSink::AddStructureChangedEvent


## -description

Raises an event to notify clients that the structure of the UI Automation tree has changed.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

A pointer to the provider of the element that is raising the event.

### -param structureChangeType [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-structurechangetype">StructureChangeType</a></b>

The type of structure change that occurred.

### -param runtimeId [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

A pointer to the runtime identifiers of the elements that are affected. These IDs enable applications to identify elements that have been removed and are no longer represented by <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a> interfaces.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iproxyproviderwineventsink">IProxyProviderWinEventSink</a>



<b>Reference</b>