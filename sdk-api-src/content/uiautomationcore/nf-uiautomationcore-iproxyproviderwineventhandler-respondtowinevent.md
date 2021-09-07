---
UID: NF:uiautomationcore.IProxyProviderWinEventHandler.RespondToWinEvent
title: IProxyProviderWinEventHandler::RespondToWinEvent (uiautomationcore.h)
description: Handles a WinEvent.
helpviewer_keywords: ["IProxyProviderWinEventHandler interface [Windows Accessibility]","RespondToWinEvent method","IProxyProviderWinEventHandler.RespondToWinEvent","IProxyProviderWinEventHandler::RespondToWinEvent","RespondToWinEvent","RespondToWinEvent method [Windows Accessibility]","RespondToWinEvent method [Windows Accessibility]","IProxyProviderWinEventHandler interface","uiauto.uiauto_IProxyProviderWinEventHandler_RespondToWinEvent","uiauto_IProxyProviderWinEventHandler_RespondToWinEvent","uiautomationcore/IProxyProviderWinEventHandler::RespondToWinEvent","winauto.uiauto_IProxyProviderWinEventHandler_RespondToWinEvent"]
old-location: winauto\uiauto_IProxyProviderWinEventHandler_RespondToWinEvent.htm
tech.root: WinAuto
ms.assetid: b3a63cb9-3eae-43ec-aba1-2f038ca0896f
ms.date: 12/05/2018
ms.keywords: IProxyProviderWinEventHandler interface [Windows Accessibility],RespondToWinEvent method, IProxyProviderWinEventHandler.RespondToWinEvent, IProxyProviderWinEventHandler::RespondToWinEvent, RespondToWinEvent, RespondToWinEvent method [Windows Accessibility], RespondToWinEvent method [Windows Accessibility],IProxyProviderWinEventHandler interface, uiauto.uiauto_IProxyProviderWinEventHandler_RespondToWinEvent, uiauto_IProxyProviderWinEventHandler_RespondToWinEvent, uiautomationcore/IProxyProviderWinEventHandler::RespondToWinEvent, winauto.uiauto_IProxyProviderWinEventHandler_RespondToWinEvent
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
 - IProxyProviderWinEventHandler::RespondToWinEvent
 - uiautomationcore/IProxyProviderWinEventHandler::RespondToWinEvent
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
 - IProxyProviderWinEventHandler.RespondToWinEvent
---

# IProxyProviderWinEventHandler::RespondToWinEvent


## -description

Handles a WinEvent.

## -parameters

### -param idWinEvent [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

The identifier of the incoming WinEvent. For a list of WinEvent IDs, see <a href="/windows/desktop/WinAuto/event-constants">Event Constants</a>.

### -param hwnd [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle of the window for which the WinEvent was fired. This should also be the window for which the proxy was created.

### -param idObject [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The object identifier (OBJID_*) of the accessible object associated with the event. For a list of object identifiers, see <a href="/windows/desktop/WinAuto/object-identifiers">Object Identifiers</a>.

### -param idChild [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LONG</a></b>

The child identifier of the element associated with the event, or <b>CHILDID_SELF</b> if the element is not a child.

### -param pSink [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iproxyproviderwineventsink">IProxyProviderWinEventSink</a>*</b>

A pointer to the <a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iproxyproviderwineventsink">IProxyProviderWinEventSink</a> interface provided by the UI Automation core. Any event that the proxy needs to raise in response to the WinEvent being handled should be added to the sink.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The provider should review the event data. If the provider needs to raise a UI Automation event in response, the data for that event should be added to the <i>pSink</i> event sink.

## -see-also

<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iproxyproviderwineventhandler">IProxyProviderWinEventHandler</a>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iproxyproviderwineventsink">IProxyProviderWinEventSink</a>


<b>Reference</b>

