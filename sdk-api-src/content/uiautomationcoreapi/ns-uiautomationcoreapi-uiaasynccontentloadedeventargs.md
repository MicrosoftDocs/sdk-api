---
UID: NS:uiautomationcoreapi.UiaAsyncContentLoadedEventArgs
title: UiaAsyncContentLoadedEventArgs (uiautomationcoreapi.h)

description: Note  This structure is deprecated.  Contains information about an event raised when content is being asynchronously loaded by a UI element.
old-location: winauto\uiauto_UiaAsyncContentLoadedEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: 070b79f2-8ed7-4bb3-85ce-a946b7cf0e6e

ms.date: 12/05/2018
ms.keywords: UiaAsyncContentLoadedEventArgs, UiaAsyncContentLoadedEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaAsyncContentLoadedEventArgsStruct, uiauto_UiaAsyncContentLoadedEventArgsStruct, uiautomationcoreapi/UiaAsyncContentLoadedEventArgs, winauto.uiauto_UiaAsyncContentLoadedEventArgsStruct
ms.topic: struct
f1_keywords: 
 - "uiautomationcoreapi/UiaAsyncContentLoadedEventArgs"
dev_langs:
 - c++
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
 - UiaAsyncContentLoadedEventArgs
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UiaAsyncContentLoadedEventArgs structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains information about an event raised when content is being asynchronously loaded by a UI element.


## -struct-fields




### -field Type

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a></b>

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a> enumerated type indicating the type of the event.


### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="https://docs.microsoft.com/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.


### -field AsyncContentLoadedState

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-asynccontentloadedstate">AsyncContentLoadedState</a></b>

A value from the <a href="https://docs.microsoft.com/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-asynccontentloadedstate">AsyncContentLoadedState</a> enumerated type indicating the state of asynchronous loading.


### -field PercentComplete

Type: <b>double</b>

The percentage of loading that has been completed.

