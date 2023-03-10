---
UID: NF:uiautomationcore.IProxyProviderWinEventSink.AddAutomationEvent
title: IProxyProviderWinEventSink::AddAutomationEvent (uiautomationcore.h)
description: Raises a Microsoft UI Automation event.
helpviewer_keywords: ["AddAutomationEvent","AddAutomationEvent method [Windows Accessibility]","AddAutomationEvent method [Windows Accessibility]","IProxyProviderWinEventSink interface","IProxyProviderWinEventSink interface [Windows Accessibility]","AddAutomationEvent method","IProxyProviderWinEventSink.AddAutomationEvent","IProxyProviderWinEventSink::AddAutomationEvent","uiauto.uiauto_IProxyProviderWinEventSink_AddAutomationEvent","uiauto_IProxyProviderWinEventSink_AddAutomationEvent","uiautomationcore/IProxyProviderWinEventSink::AddAutomationEvent","winauto.uiauto_IProxyProviderWinEventSink_AddAutomationEvent"]
old-location: winauto\uiauto_IProxyProviderWinEventSink_AddAutomationEvent.htm
tech.root: WinAuto
ms.assetid: c1730b6b-f399-4e1f-91d4-5d5e40835a74
ms.date: 12/05/2018
ms.keywords: AddAutomationEvent, AddAutomationEvent method [Windows Accessibility], AddAutomationEvent method [Windows Accessibility],IProxyProviderWinEventSink interface, IProxyProviderWinEventSink interface [Windows Accessibility],AddAutomationEvent method, IProxyProviderWinEventSink.AddAutomationEvent, IProxyProviderWinEventSink::AddAutomationEvent, uiauto.uiauto_IProxyProviderWinEventSink_AddAutomationEvent, uiauto_IProxyProviderWinEventSink_AddAutomationEvent, uiautomationcore/IProxyProviderWinEventSink::AddAutomationEvent, winauto.uiauto_IProxyProviderWinEventSink_AddAutomationEvent
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
 - IProxyProviderWinEventSink::AddAutomationEvent
 - uiautomationcore/IProxyProviderWinEventSink::AddAutomationEvent
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
 - IProxyProviderWinEventSink.AddAutomationEvent
---

# IProxyProviderWinEventSink::AddAutomationEvent


## -description

Raises a Microsoft UI Automation event.

## -parameters

### -param pProvider [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

A pointer to the provider for the element that will raise the event.

### -param id [in]

Type: <b>EVENTID</b>

The identifier of the event that will be raised. For a list of event identifiers, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iproxyproviderwineventsink">IProxyProviderWinEventSink</a>