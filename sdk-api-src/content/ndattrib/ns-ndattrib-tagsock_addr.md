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

# tagSOCK_ADDR structure


## -description


The <b>DIAG_SOCKADDR</b> structure stores an 
   Internet Protocol (IP) address for a computer that is participating in a Windows Sockets 
   communication.


## -struct-fields




### -field family

Type: <b>USHORT</b>

Socket address group.


### -field data

Type: <b>CHAR[126]</b>

The maximum size of all the different socket address structures.


## -remarks



This data structure is designed to be used as a 
    <b>SOCKADDR</b> structure.



