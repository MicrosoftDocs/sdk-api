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

# TRefPointerCollection::GetNext


## -description


<p class="CCE_Message">[The <a href="https://msdn.microsoft.com/a2d1758a-4a7e-40fd-84c7-a25bc36ab538">TRefPointerCollection</a> class 
    is part of the WMI Provider Framework which is now considered in final state, and no further development, 
    enhancements, or updates will be available for non-security related issues affecting these libraries. The 
    <a href="https://msdn.microsoft.com/7F311E1B-5CE6-488D-9411-DE1822D95C3B">MI APIs</a> should be used for all new 
    development.]

The <b>GetNext</b> method gets a pointer to the next instance in the collection.


## -parameters




### -param pos [ref]

Denotes the position of an item in a <a href="https://msdn.microsoft.com/a2d1758a-4a7e-40fd-84c7-a25bc36ab538">TRefPointerCollection</a> collection.


## -returns



The <b>GetNext</b> method returns the address of the next item by position in the <a href="https://msdn.microsoft.com/a2d1758a-4a7e-40fd-84c7-a25bc36ab538">TRefPointerCollection</a> collection.



