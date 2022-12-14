---
UID: NC:uiautomationcoreapi.UiaEventCallback
title: UiaEventCallback (uiautomationcoreapi.h)
description: A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.
helpviewer_keywords: ["UiaEventCallback","UiaEventCallback callback","UiaEventCallback callback function [Windows Accessibility]","uiauto.uiauto_UiaEventCallbackClientEvent","uiauto_UiaEventCallbackClientEvent","uiautomationcoreapi/UiaEventCallback","winauto.uiauto_UiaEventCallbackClientEvent"]
old-location: winauto\uiauto_UiaEventCallbackClientEvent.htm
tech.root: WinAuto
ms.assetid: a7dbe077-e059-4e92-8fb8-950cb67c4975
ms.date: 12/05/2018
ms.keywords: UiaEventCallback, UiaEventCallback callback, UiaEventCallback callback function [Windows Accessibility], uiauto.uiauto_UiaEventCallbackClientEvent, uiauto_UiaEventCallbackClientEvent, uiautomationcoreapi/UiaEventCallback, winauto.uiauto_UiaEventCallbackClientEvent
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
 - UiaEventCallback
 - uiautomationcoreapi/UiaEventCallback
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - UIAutomationCoreApi.h
api_name:
 - UiaEventCallback
---

# UiaEventCallback callback function


## -description

<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.

## -parameters

### -param pArgs [in]

Type: <b><a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiaeventargs">UiaEventArgs</a>*</b>

The address of a <a href="/windows/desktop/api/uiautomationcoreapi/ns-uiautomationcoreapi-uiaeventargs">UiaEventArgs</a> structure that contains the event arguments.

### -param pRequestedData [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

A <a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> that contains data associated with the event.

### -param pTreeStructure [in]

Type: <b>BSTR</b>

A string that contains the structure of the tree associated with the event, if the event is associated with a set of nodes. See Remarks.

## -remarks

This function is passed to <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaaddevent">UiaAddEvent</a> and <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaremoveevent">UiaRemoveEvent</a>.

The tree structure is described by a string where every character is either "p" or ")". The first character in the string always represents the root node. The string is <b>NULL</b> if no elements are returned by the function. 

A "p" represents a node (UI Automation element). When one "p" directly follows another, the second node is a child of the first. A ")" represents a step back up the tree. For example, "pp)p" represents a node followed by two child nodes that are siblings of one another. In "pp))p", the last node is a sibling of the first one.
