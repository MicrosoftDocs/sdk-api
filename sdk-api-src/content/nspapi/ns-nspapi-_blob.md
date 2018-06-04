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

# _BLOB structure


## -description



			The 
<b>BLOB</b> structure, derived from Binary Large Object, contains information about a block of data.


## -struct-fields




### -field cbSize

Size of the block of data pointed to by <b>pBlobData</b>, in bytes.


### -field pBlobData.size_is

 


### -field pBlobData.size_is.cbSize

 


### -field pBlobData

Pointer to a block of data.


## -remarks



The structure name 
<b>BLOB</b> comes from the acronym BLOB, which stands for Binary Large Object.

This structure does not describe the nature of the data pointed to by <b>pBlobData</b>.

<div class="alert"><b>Note</b>  Windows Sockets defines a similar 
<b>BLOB</b> structure in Wtypes.h. Using both header files in the same source code file creates redefinition–compile time errors.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/d71f3661-0efb-4376-966c-fb5c340ce1c5">Bluetooth and BLOB</a>



<a href="https://msdn.microsoft.com/e76e0c1b-8cbf-45ad-a685-fb672801c24d">SERVICE_INFO</a>
 

 

