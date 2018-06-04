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

# lineforwardlist_tag structure


## -description


The 
<b>LINEFORWARDLIST</b> structure describes a list of forwarding instructions. This structure can contain an array of 
<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a> structures. The 
<a href="https://msdn.microsoft.com/68dc99c5-1158-4e18-8e32-08216ff3567b">lineForward</a> and 
<a href="https://msdn.microsoft.com/fd70bf7f-653c-47db-bf81-6a620f47e5bc">TSPI_lineForward</a> functions use the 
<b>LINEFORWARDLIST</b> structure.


## -struct-fields




### -field dwTotalSize

Total size of the data structure, in bytes.


### -field dwNumEntries

Number of entries in the array specified as <b>ForwardList[]</b>.


### -field ForwardList

Array of forwarding instruction. The array's entries are of type 
<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a>.


## -remarks



This structure may not be extended.

The 
<b>LINEFORWARDLIST</b> structure defines the forwarding parameters requested for forwarding calls on an address or on all addresses on a line.




## -see-also




<a href="https://msdn.microsoft.com/cbdb4409-a51a-4ddf-b3ec-c5b958fc2527">LINEFORWARD</a>



<a href="https://msdn.microsoft.com/fd70bf7f-653c-47db-bf81-6a620f47e5bc">TSPI_lineForward</a>



<a href="https://msdn.microsoft.com/68dc99c5-1158-4e18-8e32-08216ff3567b">lineForward</a>
 

 

