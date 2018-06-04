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

# _IP4_ARRAY structure


## -description


The <b>IP4_ARRAY</b> structure stores an array of IPv4 addresses.


## -struct-fields




### -field AddrCount

The number of IPv4 addresses in <b>AddrArray</b>.


### -field AddrArray.size_is

 


### -field AddrArray.size_is.AddrCount

 


### -field AddrArray

An array of <a href="https://msdn.microsoft.com/652012a5-e45d-4ea6-896a-17e8b1ed4a05">IP4_ADDRESS</a> data types that contains a list of IPv4 address.

