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

# GetDotStuffState function


## -description


Determines whether dots are added to the file when any dot stuffing mechanisms are turned on.


## -parameters




### -param pContext [in]

A pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure.


### -param fReads [in]

Indicates the dot stuff states that resulted from reads or from writes. If <b>TRUE</b>, the states of Reads are provided. If <b>FALSE</b>, the states of Writes are provided.


### -param pfStuffed [out]

Indicates whether any dots were processed, scanned, or modified. If no dots were processed, scanned, or modified, this value is <b>FALSE</b>; otherwise, it is <b>TRUE</b>. 

<div class="alert"><b>Note</b>  This parameter cannot be set to <b>NULL</b>.</div>
<div> </div>

### -param pfStoredWithDots [out]

Indicates whether the file was stored with stuffed dots.


## -returns



Returns <b>TRUE</b> if the dot stuff state is known; otherwise, it returns <b>FALSE</b>.




## -remarks



The information about dot stuffing is provided by DOT_STUFF_MANAGER objects.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

