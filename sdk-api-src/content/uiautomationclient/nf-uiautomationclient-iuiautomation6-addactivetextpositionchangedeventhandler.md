---
UID: NF:uiautomationclient.IUIAutomation6.AddActiveTextPositionChangedEventHandler
title: IUIAutomation6::AddActiveTextPositionChangedEventHandler
author: windows-sdk-content
description: Registers a method that handles when the active text position changes.
old-location: winauto\uiauto_IUIAutomation6_AddActiveTextPositionChangedEventHandler.htm
tech.root: WinAuto
ms.assetid: 05D46393-6B76-415A-A1F9-F28B5DAF2074
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AddActiveTextPositionChangedEventHandler, AddActiveTextPositionChangedEventHandler method [Windows Accessibility], AddActiveTextPositionChangedEventHandler method [Windows Accessibility],IUIAutomation6 interface, IUIAutomation6 interface [Windows Accessibility],AddActiveTextPositionChangedEventHandler method, IUIAutomation6.AddActiveTextPositionChangedEventHandler, IUIAutomation6::AddActiveTextPositionChangedEventHandler, uiautomationclient/IUIAutomation6::AddActiveTextPositionChangedEventHandler, winauto.uiauto_IUIAutomation6_AddActiveTextPositionChangedEventHandler
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomation6.AddActiveTextPositionChangedEventHandler
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation6::AddActiveTextPositionChangedEventHandler


## -description


Registers a method that handles when the active text position changes.
<div class="alert"><b>Important</b>  Microsoft UI Automation clients should use the <a href="https://msdn.microsoft.com/4D92FFD9-1E83-4DE3-B20C-5203E4D7E3A2">IUIAutomationEventHandlerGroup</a> methods to register event listeners instead of individual event registration methods defined here and in the various <a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a> namespaces.</div><div> </div>

## -parameters




### -param element [in]

A pointer to the UI Automation element associated with the event handler.


### -param arg2 [in]

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and descendants.


### -param cacheRequest [in]

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

A pointer to the object that handles the active text position changed event.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.

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

For editable text elements, such as <a href="https://msdn.microsoft.com/2a71b92c-f57a-4c27-80b7-e1d9092f3701">Edit</a> and <a href="https://msdn.microsoft.com/dc34cc88-fd65-4c28-8a6a-ccfa6f3ac614">Rich Edit</a> controls,  you can listen for a SelectionChanged event.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomation6">IUIAutomation6</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomation6-removeactivetextpositionchangedeventhandler">RemoveActiveTextPositionChangedEventHandler</a>
 

 

