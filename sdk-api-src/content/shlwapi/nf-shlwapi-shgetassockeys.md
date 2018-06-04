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

# SHGetAssocKeys function


## -description


Retrieves an array of class subkeys associated with an <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> object.


## -parameters




### -param pqa [in]

A <a href="https://msdn.microsoft.com/8edb99d3-5860-4d78-a750-1df34cdfc313">IQueryAssociations</a> interface pointer to the object you're interested in.


### -param rgKeys [out]

A pointer to an array of <b>HKEY</b> elements that, when this function returns successfully, receives the retrived class subkeys.


### -param cKeys

The number of elements in the <i>rgKeys</i> array. If you are interested in only the primary class subkey, set this value to 1.


## -returns



The number of subkeys inserted into the array.



