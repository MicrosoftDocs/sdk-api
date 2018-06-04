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

# SYNCMGR_RESOLUTION_ABILITIES enumeration


## -description


Indicates abilities and the conflict resolution activity to follow. Used with <a href="https://msdn.microsoft.com/f178c4d9-0c83-4569-81fe-fe38ac13f0b5">ISyncMgrResolutionHandler::QueryAbilities</a>.


## -enum-fields




### -field SYNCMGR_RA_KEEPOTHER

The resolution handler supports merging items and will produce a merged file to keep.


### -field SYNCMGR_RA_KEEPRECENT

Enables methods <a href="https://msdn.microsoft.com/a2327234-4a8d-42b4-aa62-f5c286e3c24b">ISyncMgrResolutionHandler::KeepRecent</a> and <a href="https://msdn.microsoft.com/6d3e3b01-447c-4f7b-8a63-5bd9084de00a">ISyncMgrResolutionHandler::KeepOther</a> to be called.


### -field SYNCMGR_RA_REMOVEFROMSYNCSET

Enables method <a href="https://msdn.microsoft.com/3f65f844-efa2-43b9-91f2-c9c0ed4e3a9e">ISyncMgrResolutionHandler::RemoveFromSyncSet</a> to be called.


### -field SYNCMGR_RA_KEEP_SINGLE

Not used.


### -field SYNCMGR_RA_KEEP_MULTIPLE

Enables method <a href="https://msdn.microsoft.com/81be006b-4aa4-42da-ae1b-001ae92a3e9b">ISyncMgrResolutionHandler::KeepItems</a> to be called with more than one item in <i>pArray</i>.


### -field SYNCMGR_RA_VALID

A mask for valid <a href="https://msdn.microsoft.com/5a7ff366-e155-43c0-aafe-f61ad0caf550">SYNCMGR_RESOLUTION_ABILITIES</a> values.

