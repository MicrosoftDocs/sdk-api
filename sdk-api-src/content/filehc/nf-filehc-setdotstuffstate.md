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

# SetDotStuffState function


## -description


Enables dot stuffing to be set in an <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure.


## -parameters




### -param pContext [in]

A pointer to the <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure to be examined.


### -param fKnown [in]

Specifies whether the dot stuff state is known. If <b>TRUE</b>, the message requires dot stuffing and the <i>fRequiresStuffing</i> parameter becomes meaningful.


### -param fRequiresStuffing [in]

Specifies whether dot stuffing is required. If <i>fKnown</i> is  <b>TRUE</b>, <i>fRequiresStuffing</i> can be either <b>TRUE</b> or <b>FALSE</b>. If <i>fKnown</i> is <b>FALSE</b>, <i>fRequiresStuffing</i> is ignored.


## -returns



This function does not return a value.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

