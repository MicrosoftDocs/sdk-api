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

# DPA_DeletePtr function


## -description


<p class="CCE_Message">[<b>DPA_DeletePtr</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Removes an item from a dynamic pointer array (DPA). The DPA shrinks if necessary to accommodate the removed item.


## -parameters




### -param hdpa

TBD


### -param i

TBD




#### - index

Type: <b>int</b>

An index of item to be removed from DPA.


#### - pdpa

Type: <b>HDPA</b>

A handle to a DPA.


## -returns



Returns the removed item or <b>NULL</b>, if the call fails.



