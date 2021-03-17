---
UID: NS:uiautomationcoreapi.UiaEventArgs
title: UiaEventArgs (uiautomationcoreapi.h)
description: Note  This structure is deprecated.  Contains information about a Microsoft UI Automation event.
helpviewer_keywords: ["UiaEventArgs","UiaEventArgs structure [Windows Accessibility]","uiauto.uiauto_UiaEventArgsStruct","uiauto_UiaEventArgsStruct","uiautomationcoreapi/UiaEventArgs","winauto.uiauto_UiaEventArgsStruct"]
old-location: winauto\uiauto_UiaEventArgsStruct.htm
tech.root: WinAuto
ms.assetid: 7598936c-85da-40bc-8e94-94543371d915
ms.date: 12/05/2018
ms.keywords: UiaEventArgs, UiaEventArgs structure [Windows Accessibility], uiauto.uiauto_UiaEventArgsStruct, uiauto_UiaEventArgsStruct, uiautomationcoreapi/UiaEventArgs, winauto.uiauto_UiaEventArgsStruct
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
 - UiaEventArgs
 - uiautomationcoreapi/UiaEventArgs
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
 - UiaEventArgs
---

# UiaEventArgs structure


## -description

<div class="alert"><b>Note</b>  This structure is deprecated.</div><div> </div>  Contains information about a Microsoft UI Automation event.

## -struct-fields

### -field Type

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a></b>

A value from the <a href="/windows/desktop/api/uiautomationcoreapi/ne-uiautomationcoreapi-eventargstype">EventArgsType</a> enumerated type indicating the type of the event.

### -field EventId

Type: <b>int</b>

The identifier of the event. For a list of event identifiers, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.