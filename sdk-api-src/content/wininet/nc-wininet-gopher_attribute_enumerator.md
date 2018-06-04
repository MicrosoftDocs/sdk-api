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

# GOPHER_ATTRIBUTE_ENUMERATOR callback function


## -description


<p class="CCE_Message">[The <i>GopherAttributeEnumerator</i> function is available for use in the operating systems specified in the Requirements section.]

Prototype for a callback function that processes attribute information from a Gopher server. This callback function is installed by a call to the 
<a href="https://msdn.microsoft.com/c9e95532-8c65-45fb-acd0-a1f09cee2ce2">GopherGetAttribute</a> function.

The <b>GOPHER_ATTRIBUTE_ENUMERATOR</b> type defines a pointer to this callback function. <i>GopherAttributeEnumerator</i> is a placeholder for the application-defined function name.


## -parameters




### -param lpAttributeInfo

Pointer to a  <a href="https://msdn.microsoft.com/01daae8c-9080-4a8d-9f73-3e364ca868fe">GOPHER_ATTRIBUTE_TYPE</a> structure. The 
<i>lpBuffer</i> parameter of 
<a href="https://msdn.microsoft.com/c9e95532-8c65-45fb-acd0-a1f09cee2ce2">GopherGetAttribute</a> is used for storing this structure. The 
<i>lpBuffer</i> size must be equal to or greater than the value of MIN_GOPHER_ATTRIBUTE_LENGTH.


### -param dwError

Error value. This parameter is NO_ERROR if the attribute was parsed and written to the buffer successfully. If a problem was encountered, an error value is returned. 


## -returns



Return <b>TRUE</b> to continue the enumeration, or <b>FALSE</b> to stop it immediately. This function is primarily used for returning the results of a Gopher+ ASK item.




## -remarks



<div class="alert"><b>Note</b>  WinINet does not support server implementations. In addition, it should not be used from a service.  For server implementations or services use <a href="https://msdn.microsoft.com/354ab65d-5e46-451d-b36b-2f8166a1a048">Microsoft Windows HTTP Services (WinHTTP)</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/2e0da5c6-29e4-47b5-8ed2-8712c9ca2c97"> WinINet Functions</a>
 

 

