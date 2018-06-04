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

# ber_peek_tag function


## -description


The <b>ber_peek_tag</b> function returns the tag of the next element to be parsed in the supplied <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


## -parameters




### -param pBerElement [in]

Pointer to the source <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


### -param pLen [out]

Returns the length of the next element to be parsed.


## -returns



Returns the tag of the next element to be read in the <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to be read.




## -remarks



The decoding position within the <i>pBerElement</i> parameter is unchanged by this call; that is, the fact that <b>ber_peek_tag</b> has been called does not affect future use of the <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/079ac0a6-1b73-433e-88b3-1ce16ddc2851">ber_first_element</a>



<a href="https://msdn.microsoft.com/3daf33c9-730d-4032-a0fc-21de4c425209">ber_next_element</a>



<a href="https://msdn.microsoft.com/aa7548db-7752-4ce5-9f24-434abe77b000">ber_skip_tag</a>
 

 

