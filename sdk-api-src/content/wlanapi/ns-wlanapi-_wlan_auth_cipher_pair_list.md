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

# _WLAN_AUTH_CIPHER_PAIR_LIST structure


## -description


The <b>WLAN_AUTH_CIPHER_PAIR_LIST</b> structure contains a list of authentication and cipher algorithm pairs.


## -struct-fields




### -field dwNumberOfItems

Contains the number of supported auth-cipher pairs.


### -field pAuthCipherPairList.unique

 


### -field pAuthCipherPairList.size_is

 


### -field pAuthCipherPairList.size_is.dwNumberOfItems

 


### -field pAuthCipherPairList

A <a href="https://msdn.microsoft.com/library/windows/hardware/ff547659">DOT11_AUTH_CIPHER_PAIR</a> structure containing a list of auth-cipher pairs.


## -see-also




<a href="https://msdn.microsoft.com/e20eb9a3-5824-48ee-b13e-b0252bbf495e">WlanQueryInterface</a>
 

 

