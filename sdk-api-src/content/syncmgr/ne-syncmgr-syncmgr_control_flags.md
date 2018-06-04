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

# SYNCMGR_CONTROL_FLAGS enumeration


## -description


Specifies how an operation requested on certain methods of <a href="https://msdn.microsoft.com/197c4e6f-ffc4-4f19-a5bd-6859eef953c2">ISyncMgrControl</a> should be performed.


## -enum-fields




### -field SYNCMGR_CF_NONE

Perform the operation not using any of the other flags in this enumeration.


### -field SYNCMGR_CF_NOWAIT

Perform the operation asynchronously.


### -field SYNCMGR_CF_WAIT

Perform the operation synchronously.


### -field SYNCMGR_CF_NOUI

Perform the operation without asking the sync handler to display the UI during the operation.


### -field SYNCMGR_CF_VALID

A mask used to determine valid <a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a> flags.

