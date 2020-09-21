---
UID: NS:uiautomationcoreapi.UiaAsyncContentLoadedEventArgs
title: UiaAsyncContentLoadedEventArgs (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains information about an event raised when content is being asynchronously loaded by a UI element.
helpviewer_keywords: ["UiaAsyncContentLoadedEventArgs","UiaAsyncContentLoadedEventArgs structure [Windows Accessibility]","uiauto.uiauto_UiaAsyncContentLoadedEventArgsStruct","uiauto_UiaAsyncContentLoadedEventArgsStruct","uiautomationcoreapi/UiaAsyncContentLoadedEventArgs","winauto.uiauto_UiaAsyncContentLoadedEventArgsStruct"]
old-location: winauto\uiauto_UiaAsyncContentLoadedEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: 070b79f2-8ed7-4bb3-85ce-a946b7cf0e6e
ms.date: 12/05/2018
ms.keywords: UiaAsyncContentLoadedEventArgs, UiaAsyncContentLoadedEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaAsyncContentLoadedEventArgsStruct, uiauto_UiaAsyncContentLoadedEventArgsStruct, uiautomationcoreapi/UiaAsyncContentLoadedEventArgs, winauto.uiauto_UiaAsyncContentLoadedEventArgsStruct
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - UiaAsyncContentLoadedEventArgs
 - uiautomationcoreapi/UiaAsyncContentLoadedEventArgs
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaAsyncContentLoadedEventArgs
---

# UiaAsyncContentLoadedEventArgs structure


## -description

<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains information about an event raised when content is being asynchronously loaded by a UI element.

## -struct-fields

### -field Type

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a> enumerated type indicating the type of the event.

### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

### -field AsyncContentLoadedState

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-asynccontentloadedstate">AsyncContentLoadedState</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-asynccontentloadedstate">AsyncContentLoadedState</a> enumerated type indicating the state of asynchronous loading.

### -field PercentComplete

Type: <b>double</b>

The percentage of loading that has been completed.