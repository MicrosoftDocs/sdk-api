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

# _DRT_ADDRESS_FLAGS enumeration


## -description


The <b>DRT_ADDRESS_FLAGS</b> enumeration defines the set of responses that may be returned by an intermediate node when performing a search for a key.


## -enum-fields




### -field DRT_ADDRESS_FLAG_ACCEPTED

The response provided by this machine was successfully used to make progress towards the search target.


### -field DRT_ADDRESS_FLAG_REJECTED

The response provided by this machine was not used in the search.  This machine may have provided the address of a node publishing a key numerically farther from the target than other nodes already contacted.


### -field DRT_ADDRESS_FLAG_UNREACHABLE

This machine did not respond.


### -field DRT_ADDRESS_FLAG_LOOP

The response provided by this machine was not used in the search.  This machine provided the address of a node that has already been contacted.


### -field DRT_ADDRESS_FLAG_TOO_BUSY

This machine indicated that it does not have sufficient resources to process the query.


### -field DRT_ADDRESS_FLAG_BAD_VALIDATE_ID

This machine is not publishing the key expected by the local DRT instance.  As a result, it may not be able to provide useful information.


### -field DRT_ADDRESS_FLAG_SUSPECT_UNREGISTERED_ID

This machine has reason to believe that the target key has been unregistered.


### -field DRT_ADDRESS_FLAG_INQUIRE

This machine was asked to provide proof of ownership of its key.

