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

# tagExtendedIsolationState enumeration


## -description


<div class="alert"><b>Note</b>  The Network Access Protection platform is not available starting with Windows 10</div><div> </div>The <b>ExtendedIsolationState</b> enumeration describes the extended isolation state of a connection.


## -enum-fields




### -field extendedIsolationStateNoData

No data is available on the connection isolation state.


### -field extendedIsolationStateTransition

The connection isolation state is "transition".


### -field extendedIsolationStateInfected

The connection isolation state is "infected".


### -field extendedIsolationStateUnknown

The connection isolation state is unknown.

