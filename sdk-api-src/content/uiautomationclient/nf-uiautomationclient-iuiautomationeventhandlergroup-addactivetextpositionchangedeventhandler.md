---
UID: NF:uiautomationclient.IUIAutomationEventHandlerGroup.AddActiveTextPositionChangedEventHandler
title: IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler (uiautomationclient.h)
description: Registers a method (in an event handler group) that handles when the active text position changes.
helpviewer_keywords: ["AddActiveTextPositionChangedEventHandler","AddActiveTextPositionChangedEventHandler method [Windows Accessibility]","AddActiveTextPositionChangedEventHandler method [Windows Accessibility]","IUIAutomationEventHandlerGroup interface","IUIAutomationEventHandlerGroup interface [Windows Accessibility]","AddActiveTextPositionChangedEventHandler method","IUIAutomationEventHandlerGroup.AddActiveTextPositionChangedEventHandler","IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler","uiautomationclient/IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler","winauto.uiauto_IUIAutomationEventHandlerGroup_AddActiveTextPositionChangedEventHandler"]
old-location: winauto\uiauto_IUIAutomationEventHandlerGroup_AddActiveTextPositionChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: D3A09F61-5536-409E-BFA2-63D6E4A774A2
ms.date: 12/05/2018
ms.keywords: AddActiveTextPositionChangedEventHandler, AddActiveTextPositionChangedEventHandler method [Windows Accessibility], AddActiveTextPositionChangedEventHandler method [Windows Accessibility],IUIAutomationEventHandlerGroup interface, IUIAutomationEventHandlerGroup interface [Windows Accessibility],AddActiveTextPositionChangedEventHandler method, IUIAutomationEventHandlerGroup.AddActiveTextPositionChangedEventHandler, IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler, uiautomationclient/IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler, winauto.uiauto_IUIAutomationEventHandlerGroup_AddActiveTextPositionChangedEventHandler
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
 - IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler
 - uiautomationclient/IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler
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
 - IUIAutomationEventHandlerGroup.AddActiveTextPositionChangedEventHandler
---

# IUIAutomationEventHandlerGroup::AddActiveTextPositionChangedEventHandler


## -description

Registers a method (in an event handler group) that handles when the active text position changes.<div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the handler group methods to register event listeners instead of individual event registration methods defined in the various <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation">IUIAutomation</a> namespaces.</div>
<div> </div>

## -parameters

### -param scope [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.

### -param cacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.

### -param handler [in]

A pointer to the object that handles the active text position changed event.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before implementing an event handler, you should be familiar with the threading issues described in <a href="/windows/desktop/WinAuto/uiauto-threading">Understanding Threading Issues</a>.

Active text position is indicated by a navigation event within or between read-only text elements (such as web browsers, Portable Document Format (PDF) documents, or <a href="https://en.wikipedia.org/wiki/EPUB">EPUB</a> documents) using  bookmarks (or fragment identifiers to refer to a location within a resource). Examples include:

<ul>
<li>Navigating to a bookmark within the same web page</li>
<li>Navigating to a bookmark on a different web page </li>
<li>Activating a link to a different location within the same PDF</li>
<li>Activating a link to a different location within the same <a href="https://en.wikipedia.org/wiki/EPUB">EPUB</a></li>
</ul>
Use this event handler to sync the visual location of the bookmark/target with the focus location in a read-only text element, which can diverge when using bookmarks or fragment identifiers.

 For example, when a same page anchor (<code>&lt;a href=”#C4”&gt;Jump to Chapter 4&lt;/a&gt; ... &lt;h1&gt;&lt;a name="C4"&gt;Chapter 4&lt;/a&gt;&lt;/h1&gt;</code>) 
is invoked, the visual location is updated, but the UI Automation client remains at the original location. This results in actions such as text reading or move next item commands starting from the original location, not the new location. 

Similarly, activating a new page URI (with a fragment identifier: (<code>&lt;a href=”www.blah.com#C4”&gt;Jump to Chapter 4&lt;/a&gt;</code>)) loads the new page and jumps to the specified bookmark, but leaves the UI Automation clients   at the top of the page.

For editable text elements, such as <a href="/windows/desktop/controls/edit-controls">Edit</a> and <a href="/windows/desktop/controls/rich-edit-controls">Rich Edit</a> controls,  you can listen for a SelectionChanged event.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationeventhandlergroup">IUIAutomationEventHandlerGroup</a>