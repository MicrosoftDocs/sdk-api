---
UID: NS:uiautomationcoreapi.UiaEventArgs
title: UiaEventArgs
author: windows-sdk-content
description: Note  This structure is deprecated.  Contains information about a Microsoft UI Automation event.
old-location: winauto\uiauto_UiaEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: 7598936c-85da-40bc-8e94-94543371d915
ms.author: windowssdkdev
ms.date: 10/23/2018
ms.keywords: UiaEventArgs, UiaEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaEventArgsStruct, uiauto_UiaEventArgsStruct, uiautomationcoreapi/UiaEventArgs, winauto.uiauto_UiaEventArgsStruct
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
 - UiaEventArgs
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UiaEventArgs structure


## -description


<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains information about a Microsoft UI Automation event.


## -struct-fields




### -field Type

Type: <b><a href="https://msdn.microsoft.com/b62712cc-bb00-44b0-9664-cc8edbfabb0a">EventArgsType</a></b>

A value from the <a href="https://msdn.microsoft.com/b62712cc-bb00-44b0-9664-cc8edbfabb0a">EventArgsType</a> enumerated type indicating the type of the event.


### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="https://msdn.microsoft.com/4baf5cb9-c965-4977-ae2b-420e84dc2e94">Event Identifiers</a>.

