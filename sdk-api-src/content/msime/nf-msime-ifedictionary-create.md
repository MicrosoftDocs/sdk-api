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

# IFEDictionary::Create


## -description


Creates a new dictionary file.


## -parameters




### -param pchDictPath [in]

A <b>NULL</b>-terminated string containing the path and name for the new dictionary file to be created.


### -param pshf [in]

The <a href="https://msdn.microsoft.com/CFFEFEDC-F614-4DD4-B1A1-4D236339E817">IMESHF</a> header for the new dictionary.


## -returns



One of the following:

<ul>
<li><b>S_OK</b></li>
<li><b>IFED_S_EMPTY_DICTIONARY</b></li>
<li><b>E_OUTOFMEMORY</b></li>
<li><b>E_FAIL</b></li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4C63FF43-0170-4038-AB01-72441E1BB189">IFEDictionary</a>



<a href="https://msdn.microsoft.com/CFFEFEDC-F614-4DD4-B1A1-4D236339E817">IMESHF</a>
 

 

