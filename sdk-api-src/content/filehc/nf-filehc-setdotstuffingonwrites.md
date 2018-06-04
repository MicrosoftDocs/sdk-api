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

# SetDotStuffingOnWrites function


## -description


Enables dot-stuffing properties on the write path of the file handle cache of the message.


## -parameters




### -param pContext [in]

A pointer to an <a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a> structure that contains context information.


### -param fEnable [in]

Specifies whether dot stuffing is available. If <b>FALSE</b>, all dot-stuffing behavior is turned off.


### -param fStripDots [in]

Specifies whether occurrences of "\r\n." are converted to "\r\n" within the message. If <b>TRUE</b>,  "\r\n." is converted to "\r\n" (unstuffing or stripping). If  <b>FALSE</b>,   "\r\n." is converted to "\r\n.." (stuffing).


## -returns



Returns <b>TRUE</b> if the function succeeds; otherwise, it is <b>FALSE</b>.




## -see-also




<a href="Http://go.microsoft.com/fwlink/p/?linkid=85304">FIO_CONTEXT</a>
 

 

