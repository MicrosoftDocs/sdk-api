---
UID: NF:uiautomationclient.IUIAutomation4.AddChangesEventHandler
title: IUIAutomation4::AddChangesEventHandler (uiautomationclient.h)
description: Registers a method that handles change events.Note  Before implementing an event handler, you should be familiar with the threading issues described in Understanding Threading Issues.
helpviewer_keywords: ["AddChangesEventHandler","AddChangesEventHandler method [Windows Accessibility]","AddChangesEventHandler method [Windows Accessibility]","IUIAutomation4 interface","IUIAutomation4 interface [Windows Accessibility]","AddChangesEventHandler method","IUIAutomation4.AddChangesEventHandler","IUIAutomation4::AddChangesEventHandler","uiautomationclient/IUIAutomation4::AddChangesEventHandler","winauto.uiauto_IUIAutomation4_AddChangesEventHandler"]
old-location: winauto\uiauto_IUIAutomation4_AddChangesEventHandler.htm
tech.root: WinAuto
ms.assetid: E479ACCA-9372-463F-A992-8030E33A2341
ms.date: 12/05/2018
ms.keywords: AddChangesEventHandler, AddChangesEventHandler method [Windows Accessibility], AddChangesEventHandler method [Windows Accessibility],IUIAutomation4 interface, IUIAutomation4 interface [Windows Accessibility],AddChangesEventHandler method, IUIAutomation4.AddChangesEventHandler, IUIAutomation4::AddChangesEventHandler, uiautomationclient/IUIAutomation4::AddChangesEventHandler, winauto.uiauto_IUIAutomation4_AddChangesEventHandler
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomation4::AddChangesEventHandler
 - uiautomationclient/IUIAutomation4::AddChangesEventHandler
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation4.AddChangesEventHandler
---

# IUIAutomation4::AddChangesEventHandler


## -description

Registers a method that handles change events.
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.</div><div> </div>

## -parameters

### -param element [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.

### -param scope [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.

### -param changeTypes [in]

Type: <b>int*</b>

A pointer to a list of integers that indicate the change types the event represents.

### -param changesCount [in]

Type: <b>int</b>

The number of changes that occurred in this event.

### -param pCacheRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationcacherequest">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationchangeseventhandler">IUIAutomationChangesEventHandler</a>*</b>

A pointer to the object that handles the changes event.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

A Microsoft UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation4">IUIAutomation4</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation-removealleventhandlers">RemoveAllEventHandlers</a>