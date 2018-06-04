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

# IDListContainerIsConsistent function


## -description


Verifies that the container structure of an IDList is valid.


## -parameters




### -param pidl [in]

A pointer to the IDList to validate.


### -param cbAlloc [in]

The size, in bytes, of the PIDL specified in the <i>pidl</i> parameter.


## -returns



<b>TRUE</b> if the IDList structure is valid; otherwise, <b>FALSE</b>.




## -remarks



This function should be used by any code that reads an IDList from a persisted format to ensure that invalid forms do not lead to a security exploit in the code that interprets the IDList. Shell data sources are responsible for validating private sections of the ITEMIDs. Hidden data is validated by the functions that interpret that data.



