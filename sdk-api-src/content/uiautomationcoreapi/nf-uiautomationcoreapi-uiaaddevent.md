---
UID: NF:uiautomationcoreapi.UiaAddEvent
title: UiaAddEvent function (uiautomationcoreapi.h)
description: Adds a listener for events on a node in the UI Automation tree.
helpviewer_keywords: ["UiaAddEvent","UiaAddEvent function [Windows Accessibility]","uiauto.uiauto_UiaAddEventClientEvent","uiauto_UiaAddEventClientEvent","uiautomationcoreapi/UiaAddEvent","winauto.uiauto_UiaAddEventClientEvent"]
old-location: winauto\uiauto_UiaAddEventClientEvent.htm
tech.root: WinAuto
ms.assetid: 6d53c864-2791-4693-84dd-c7c1d8262b1f
ms.date: 12/05/2018
ms.keywords: UiaAddEvent, UiaAddEvent function [Windows Accessibility], uiauto.uiauto_UiaAddEventClientEvent, uiauto_UiaAddEventClientEvent, uiautomationcoreapi/UiaAddEvent, winauto.uiauto_UiaAddEventClientEvent
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaAddEvent
 - uiautomationcoreapi/UiaAddEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Uiautomationcore.dll
api_name:
 - UiaAddEvent
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

The identifier of the event to listen for. For a list of event IDs, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

### -param pCallback [in]

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/nc-uiautomationcoreapi-uiaeventcallback">UiaEventCallback</a>*</b>

The address of the application-defined <a href="/windows/desktop/api/uiautomationcoreapi/nc-uiautomationcoreapi-uiaeventcallback">UiaEventCallback</a> callback function that is called when the event is raised.

### -param scope [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a>*</b>

A value from the <a href="/windows/desktop/api/uiautomationclient/ne-uiautomationclient-treescope">TreeScope</a> enumerated type indicating the scope of events to be handled; that is, whether they are on the element itself, 
				or on its ancestors and children.

### -param pProperties [in]

Type: <b>PROPERTYID*</b>

The address of an array that contains the identifiers of the properties to monitor for change events, when <i>eventId</i> is the EVENTID derived from AutomationPropertyChanged_Event_GUID; otherwise this parameter is <b>NULL</b>. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param cProperties [in]

Type: <b>int</b>

The count of elements in the <i>pProperties</i> array.

### -param pRequest [in]

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacacherequest">UiaCacheRequest</a>*</b>

The address of a <a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiacacherequest">UiaCacheRequest</a> structure that defines the cache request in effect for nodes that are returned with events.

### -param phEvent [out]

Type: <b>HUIEVENT*</b>

When this function returns, contains 
				a pointer to the event that is added. 
				This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful or an error value otherwise.

## -see-also

<a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uialookupid">UiaLookupId</a>