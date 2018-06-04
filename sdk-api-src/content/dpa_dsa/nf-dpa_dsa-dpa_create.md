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

# DPA_Create function


## -description


<p class="CCE_Message">[<b>DPA_Create</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Creates a dynamic pointer array (DPA).


## -parameters




### -param cItemGrow

TBD




#### - cpGrow

Type: <b>int</b>

The number of elements by which the array should be expanded, if the DPA needs to be enlarged.


## -returns



Type: <b>HDPA</b>

Returns a handle to a DPA if successful, or <b>NULL</b> if the call fails.




## -see-also




<a href="https://msdn.microsoft.com/a77ad74e-3bb5-414a-9cd7-db4b1c6e8116">DPA_CreateEx</a>
 

 

