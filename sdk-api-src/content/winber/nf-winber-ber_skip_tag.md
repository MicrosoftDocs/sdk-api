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

# ber_skip_tag function


## -description


The <b>ber_skip_tag</b> function skips  the current tag and returns the tag of the next element in the supplied <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


## -parameters




### -param pBerElement [in]

Pointer to the source <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure.


### -param pLen [out]

Returns the length of the skipped element.


## -returns



Returns the tag of the next element in the <a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> structure. LBER_DEFAULT is returned if there is no further data to read.




## -remarks



This function is similar to 
<a href="https://msdn.microsoft.com/0c6f24fa-47df-401c-afe8-84bf2987dd36">ber_peek_tag</a>, except that the state pointer, in the 
<a href="https://msdn.microsoft.com/491bdf54-0b45-4324-93fc-35fe15155a3d">BerElement</a> argument, is advanced past the first tag and length, and is pointed to the value part of the next element. This routine should only be used with constructed types and situations when a BER encoding is used as the value of an OCTET STRING.




## -see-also




<a href="https://msdn.microsoft.com/079ac0a6-1b73-433e-88b3-1ce16ddc2851">ber_first_element</a>



<a href="https://msdn.microsoft.com/3daf33c9-730d-4032-a0fc-21de4c425209">ber_next_element</a>



<a href="https://msdn.microsoft.com/0c6f24fa-47df-401c-afe8-84bf2987dd36">ber_peek_tag</a>
 

 

