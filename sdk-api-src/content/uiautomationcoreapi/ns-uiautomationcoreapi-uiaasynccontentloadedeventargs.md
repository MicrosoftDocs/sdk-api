---
UID: NS:uiautomationcoreapi.UiaAsyncContentLoadedEventArgs
title: UiaAsyncContentLoadedEventArgs
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains information about an event raised when content is being asynchronously loaded by a UI element.
old-location: winauto\uiauto_UiaAsyncContentLoadedEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: 070b79f2-8ed7-4bb3-85ce-a946b7cf0e6e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: UiaAsyncContentLoadedEventArgs, UiaAsyncContentLoadedEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaAsyncContentLoadedEventArgsStruct, uiauto_UiaAsyncContentLoadedEventArgsStruct, uiautomationcoreapi/UiaAsyncContentLoadedEventArgs, winauto.uiauto_UiaAsyncContentLoadedEventArgsStruct
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaAsyncContentLoadedEventArgs structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains information about an event raised when content is being asynchronously loaded by a UI element.


## -struct-fields




### -field Type

Type: <b><a href="https://msdn.microsoft.com/b62712cc-bb00-44b0-9664-cc8edbfabb0a">EventArgsType</a></b>

A value from the <a href="https://msdn.microsoft.com/b62712cc-bb00-44b0-9664-cc8edbfabb0a">EventArgsType</a> enumerated type indicating the type of the event.


### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.


### -field AsyncContentLoadedState

Type: <b><a href="https://msdn.microsoft.com/7c562d3a-10cc-4d9e-aaad-6729574fcb96">AsyncContentLoadedState</a></b>

A value from the <a href="https://msdn.microsoft.com/7c562d3a-10cc-4d9e-aaad-6729574fcb96">AsyncContentLoadedState</a> enumerated type indicating the state of asynchronous loading.


### -field PercentComplete

Type: <b>double</b>

The percentage of loading that has been completed.

