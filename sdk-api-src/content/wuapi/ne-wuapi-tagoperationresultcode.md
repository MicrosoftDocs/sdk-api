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

# tagOperationResultCode enumeration


## -description


Defines the possible results of a download, install, uninstall, or verification operation on an update.


## -enum-fields




### -field orcNotStarted

The operation is not started.


### -field orcInProgress

The operation is in progress.


### -field orcSucceeded

The operation was completed successfully.


### -field orcSucceededWithErrors

The operation is complete, but one or more errors occurred during the operation. The results might be incomplete.


### -field orcFailed

The operation  failed to complete.


### -field orcAborted

The operation is canceled.

