---
UID: NF:uiautomationclient.IUIAutomation6.AddActiveTextPositionChangedEventHandler
title: IUIAutomation6::AddActiveTextPositionChangedEventHandler (uiautomationclient.h)
description: Registers a method that handles when the active text position changes.
helpviewer_keywords: ["AddActiveTextPositionChangedEventHandler","AddActiveTextPositionChangedEventHandler method [Windows Accessibility]","AddActiveTextPositionChangedEventHandler method [Windows Accessibility]","IUIAutomation6 interface","IUIAutomation6 interface [Windows Accessibility]","AddActiveTextPositionChangedEventHandler method","IUIAutomation6.AddActiveTextPositionChangedEventHandler","IUIAutomation6::AddActiveTextPositionChangedEventHandler","uiautomationclient/IUIAutomation6::AddActiveTextPositionChangedEventHandler","winauto.uiauto_IUIAutomation6_AddActiveTextPositionChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomation6_AddActiveTextPositionChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 05D46393-6B76-415A-A1F9-F28B5DAF2074
ms.date: 12/05/2019
ms.keywords: AddActiveTextPositionChangedEventHandler, AddActiveTextPositionChangedEventHandler method [Windows Accessibility], AddActiveTextPositionChangedEventHandler method [Windows Accessibility],IUIAutomation6 interface, IUIAutomation6 interface [Windows Accessibility],AddActiveTextPositionChangedEventHandler method, IUIAutomation6.AddActiveTextPositionChangedEventHandler, IUIAutomation6::AddActiveTextPositionChangedEventHandler, uiautomationclient/IUIAutomation6::AddActiveTextPositionChangedEventHandler, winauto.uiauto_IUIAutomation6_AddActiveTextPositionChangedEventHandler
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server, version 1709 [desktop apps only]
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
ms.custom: RS5, 19H1
f1_keywords:
 - IUIAutomation6::AddActiveTextPositionChangedEventHandler
 - uiautomationclient/IUIAutomation6::AddActiveTextPositionChangedEventHandler
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
 - IUIAutomation6.AddActiveTextPositionChangedEventHandler
---

# IUIAutomation6::AddActiveTextPositionChangedEventHandler


## -description

Registers a method that handles when the active text position changes.

> [!Important]
> Microsoft UI Automation clients should use the [IUIAutomationEventHandlerGroup interface](nn-uiautomationclient-iuiautomationeventhandlergroup.md) methods to register event listeners instead of individual event registration methods defined here and in the various [IUIAutomation interface](nn-uiautomationclient-iuiautomation.md) namespaces.

## -parameters

### -param element [in]

A pointer to the UI Automation element associated with the event handler.

### -param scope [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.

### -param cacheRequest [in]

A pointer to a cache request, or NULL if no caching is wanted.

### -param handler [in]

A pointer to the object that handles the active text position changed event.

## -returns

If this method succeeds, it returns S_OK. Otherwise, it returns an HRESULT error code.

## -remarks

Before implementing an event handler, you should be familiar with the threading issues described in [Understanding Threading Issues](/windows/desktop/WinAuto/uiauto-threading).

Active text position is indicated by a navigation event within or between read-only text elements (such as web browsers, Portable Document Format (PDF) documents, or [EPUB](https://en.wikipedia.org/wiki/EPUB) documents) using  bookmarks (or fragment identifiers to refer to a location within a resource). Examples include:

- Navigating to a bookmark within the same web page
- Navigating to a bookmark on a different web page
- Activating a link to a different location within the same PDF
- Activating a link to a different location within the same [EPUB](https://en.wikipedia.org/wiki/EPUB)

Use this event handler to sync the visual location of the bookmark/target with the focus location in a read-only text element, which can diverge when using bookmarks or fragment identifiers.

For example, when a same page anchor (`<a href="#C4">Jump to Chapter 4</a> ...<h1><a name="C4">Chapter 4</a></h1>`) is invoked, the visual location is updated, but the UI Automation client remains at the original location. This results in actions such as text reading or move next item commands starting from the original location, not the new location.

Similarly, activating a new page URI (with a fragment identifier: (`<a href="www.blah.com#C4">Jump to Chapter 4</a>`) loads the new page and jumps to the specified bookmark, but leaves the UI Automation clients at the top of the page.

For editable text elements, such as [Edit](/windows/desktop/controls/edit-controls) and [Rich Edit](/windows/win32/controls/rich-edit-controls)controls, you can listen for a SelectionChanged event.

It is possible for an event to be delivered to an event handler after the handler has been unsubscribed, if the event is received simultaneously with the request to unsubscribe the event. The best practice is to follow the Component Object Model (COM) standard and avoid destroying the event handler object until its reference count has reached zero. Destroying an event handler immediately after unsubscribing for events may result in an access violation if an event is delivered late.

## -see-also

[IUIAutomation6::RemoveActiveTextPositionChangedEventHandler](nf-uiautomationclient-iuiautomation6-removeactivetextpositionchangedeventhandler.md), [IUIAutomation6 interface](nn-uiautomationclient-iuiautomation6.md)

