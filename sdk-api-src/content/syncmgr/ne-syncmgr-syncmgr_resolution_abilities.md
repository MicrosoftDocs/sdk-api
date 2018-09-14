---
UID: NE:syncmgr.SYNCMGR_RESOLUTION_ABILITIES
title: SYNCMGR_RESOLUTION_ABILITIES
author: windows-sdk-content
description: Indicates abilities and the conflict resolution activity to follow. Used with ISyncMgrResolutionHandler::QueryAbilities.
old-location: shell\SYNCMGR_RESOLUTION_ABILITIES.htm
tech.root: shell
ms.assetid: 5a7ff366-e155-43c0-aafe-f61ad0caf550
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: SYNCMGR_RA_KEEPOTHER, SYNCMGR_RA_KEEPRECENT, SYNCMGR_RA_KEEP_MULTIPLE, SYNCMGR_RA_KEEP_SINGLE, SYNCMGR_RA_REMOVEFROMSYNCSET, SYNCMGR_RA_VALID, SYNCMGR_RESOLUTION_ABILITIES, SYNCMGR_RESOLUTION_ABILITIES enumeration [Windows Shell], _shell_SYNCMGR_RESOLUTION_ABILITIES, shell.SYNCMGR_RESOLUTION_ABILITIES, syncmgr/SYNCMGR_RA_KEEPOTHER, syncmgr/SYNCMGR_RA_KEEPRECENT, syncmgr/SYNCMGR_RA_KEEP_MULTIPLE, syncmgr/SYNCMGR_RA_KEEP_SINGLE, syncmgr/SYNCMGR_RA_REMOVEFROMSYNCSET, syncmgr/SYNCMGR_RA_VALID, syncmgr/SYNCMGR_RESOLUTION_ABILITIES
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Syncmgr.h
api_name:
 - SYNCMGR_RESOLUTION_ABILITIES
product: Windows
targetos: Windows
req.typenames: SYNCMGR_RESOLUTION_ABILITIES
req.redist: 
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

