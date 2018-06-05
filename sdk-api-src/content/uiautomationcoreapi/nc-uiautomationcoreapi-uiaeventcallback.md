---
UID: NC:uiautomationcoreapi.UiaEventCallback
title: UiaEventCallback
author: windows-sdk-content
description: A client-implemented function that is called by UI Automation when an event is raised that the client has subscribed to.
old-location: winauto\uiauto_UiaEventCallbackClientEvent.htm
old-project: WinAuto
ms.assetid: a7dbe077-e059-4e92-8fb8-950cb67c4975
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: UiaEventCallback, UiaEventCallback callback, UiaEventCallback callback function [Windows Accessibility], uiauto.uiauto_UiaEventCallbackClientEvent, uiauto_UiaEventCallbackClientEvent, uiautomationcoreapi/UiaEventCallback, winauto.uiauto_UiaEventCallbackClientEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
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
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	UIAutomationCoreApi.h
api_name:
-	UiaEventCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# UiaEventCallback callback function


## -description


<div class="alert"><b>Note</b>  This function is deprecated. Client applications should use the Microsoft UI Automation Component Object Model (COM) interfaces instead.</div><div> </div>A client-implemented function that is called by UI Automation when 
		an event is raised that the client has subscribed to.


## -parameters




### -param *pArgs [in]

Type: <b><a href="https://msdn.microsoft.com/7598936c-85da-40bc-8e94-94543371d915">UiaEventArgs</a>*</b>

The address of a <a href="https://msdn.microsoft.com/7598936c-85da-40bc-8e94-94543371d915">UiaEventArgs</a> structure that contains the event arguments.


### -param *pRequestedData [in]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>*</b>

A <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains data associated with the event.


### -param pTreeStructure [in]

Type: <b>BSTR</b>

A string that contains the structure of the tree associated with the event, if the event 
				is associated with a set of nodes. See Remarks.


## -remarks



 This function is passed to <a href="https://msdn.microsoft.com/6d53c864-2791-4693-84dd-c7c1d8262b1f">UiaAddEvent</a> and <a href="https://msdn.microsoft.com/c98b3e0f-c3d3-45a5-b1a1-80da1b5673f3">UiaRemoveEvent</a>.

	The tree structure is described by a string where every character is either "p" or ")". 
			The first character in the string always represents the root node. The string is <b>NULL</b> if 
			no elements are returned by the function. 

A "p" represents a node (UI Automation element). When one "p" directly follows another, 
			the second node is a child of the first. A ")" represents a step back up the tree. 
			For example, "pp)p" represents a node followed by two child nodes that are siblings of one another. 
			In "pp))p", the last node is a sibling of the first one.



