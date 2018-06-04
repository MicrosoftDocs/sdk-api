---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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



