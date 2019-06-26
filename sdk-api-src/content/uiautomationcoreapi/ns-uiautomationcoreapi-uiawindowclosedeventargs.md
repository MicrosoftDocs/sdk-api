---
UID: NS:uiautomationcoreapi.UiaWindowClosedEventArgs
title: UiaWindowClosedEventArgs (uiautomationcoreapi.h)
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains information about an event that is raised when one or more windows closes.
old-location: winauto\uiauto_UiaWindowClosedEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: e15b2e58-5eba-4804-9f4a-6bba4afa2051
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: UiaWindowClosedEventArgs, UiaWindowClosedEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaWindowClosedEventArgsStruct, uiauto_UiaWindowClosedEventArgsStruct, uiautomationcoreapi/UiaWindowClosedEventArgs, winauto.uiauto_UiaWindowClosedEventArgsStruct
ms.topic: struct
f1_keywords: 
 - "uiautomationcoreapi/UiaWindowClosedEventArgs"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaWindowClosedEventArgs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UiaWindowClosedEventArgs structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div> Contains information about an event that is raised when one or more windows closes.


## -struct-fields




### -field Type

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a></b>

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a> enumerated type indicating the type of event.


### -field EventId

Type: <b>int</b>

The event identifier. For a list of event identifiers, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.


### -field pRuntimeId

Type: <b>int*</b>

The address of an array of the UI Automation runtime identifiers of windows that have closed.


### -field cRuntimeIdLen

Type: <b>int</b>

The count of elements in the array.


## -remarks



This event is raised for any window (HWND) that closes, not just top-level windows.
	



