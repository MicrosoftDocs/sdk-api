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

# FreeConfirmConflictItem function


## -description


Frees the resources that have been allocated for a <a href="https://msdn.microsoft.com/3be4a8ec-eeab-4453-a2cb-18cadf39464a">CONFIRM_CONFLICT_ITEM</a> structure.


## -parameters




### -param pcci [in, out]

Type: <b><a href="https://msdn.microsoft.com/3be4a8ec-eeab-4453-a2cb-18cadf39464a">CONFIRM_CONFLICT_ITEM</a>*</b>

A pointer to a <a href="https://msdn.microsoft.com/3be4a8ec-eeab-4453-a2cb-18cadf39464a">CONFIRM_CONFLICT_ITEM</a> structure that stores pointers to the items for which memory is to be freed.


## -returns



This function does not return a value.



