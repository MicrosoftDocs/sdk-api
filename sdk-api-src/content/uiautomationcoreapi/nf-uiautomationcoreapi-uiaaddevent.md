---
UID: NF:uiautomationcoreapi.UiaAddEvent
title: UiaAddEvent function (uiautomationcoreapi.h)
author: windows-sdk-content
description: Adds a listener for events on a node in the UI Automation tree.
old-location: winauto\uiauto_UiaAddEventClientEvent.htm
tech.root: WinAuto
ms.assetid: 6d53c864-2791-4693-84dd-c7c1d8262b1f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UiaAddEvent, UiaAddEvent function [Windows Accessibility], uiauto.uiauto_UiaAddEventClientEvent, uiauto_UiaAddEventClientEvent, uiautomationcoreapi/UiaAddEvent, winauto.uiauto_UiaAddEventClientEvent
ms.topic: function
req.header: uiautomationcoreapi.h
req.include-header: 
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
req.lib: Uiautomationcore.lib
req.dll: Uiautomationcore.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaAddEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UiaAddEvent function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>Adds a listener for events on a node in the UI Automation tree.


## -parameters




### -param hnode [in]

Type: <b>HUIANODE</b>

The node to add an event listener to.


### -param eventId [in]

Type: <b>EVENTID</b>

The identifier of the event to listen for. For a list of event IDs, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


### -param pCallback [in]

Type: <b><a href="https://msdn.microsoft.com/a7dbe077-e059-4e92-8fb8-950cb67c4975">UiaEventCallback</a>*</b>

The address of the application-defined <a href="https://msdn.microsoft.com/a7dbe077-e059-4e92-8fb8-950cb67c4975">UiaEventCallback</a> callback function that is called when the event is raised.


### -param scope [in]

Type: <b><a href="https://msdn.microsoft.com/eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e">TreeScope</a>*</b>

A value from the <a href="https://msdn.microsoft.com/eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e">TreeScope</a> enumerated type indicating the scope of events to be handled; that is, whether they are on the element itself, 
				or on its ancestors and children.


### -param pProperties [in]

Type: <b>PROPERTYID*</b>

The address of an array that contains the identifiers of the properties to monitor for change events, when <i>eventId</i> is the EVENTID derived from AutomationPropertyChanged_Event_GUID; otherwise this parameter is <b>NULL</b>. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param cProperties [in]

Type: <b>int</b>

The count of elements in the <i>pProperties</i> array.


### -param pRequest [in]

Type: <b><a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a>*</b>

The address of a <a href="https://msdn.microsoft.com/426355e4-50ce-4189-824d-c2256903224c">UiaCacheRequest</a> structure that defines the cache request in effect for nodes that are returned with events.


### -param phEvent [out]

Type: <b>HUIEVENT*</b>

When this function returns, contains 
				a pointer to the event that is added. 
				This parameter is passed uninitialized.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.




## -see-also




<a href="https://msdn.microsoft.com/9906acea-5246-4f01-8d76-03b89ff2f789">UiaLookupId</a>
 

 

