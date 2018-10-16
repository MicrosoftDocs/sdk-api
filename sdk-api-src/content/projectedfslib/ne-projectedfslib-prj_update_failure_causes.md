---
UID: NE:projectedfslib.PRJ_UPDATE_FAILURE_CAUSES
title: PRJ_UPDATE_FAILURE_CAUSES
author: windows-sdk-content
description: Descriptions for the reason an update failed.
old-location: projfs\prj_update_failure_causes.htm
tech.root: ProjFS
ms.assetid: 8C3375C5-507C-4336-8F6A-DE509F3F20D2
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: PRJ_UPDATE_FAILURE_CAUSES, PRJ_UPDATE_FAILURE_CAUSES enumeration, PRJ_UPDATE_FAILURE_CAUSE_DIRTY_DATA, PRJ_UPDATE_FAILURE_CAUSE_DIRTY_METADATA, PRJ_UPDATE_FAILURE_CAUSE_NONE, PRJ_UPDATE_FAILURE_CAUSE_READ_ONLY, PRJ_UPDATE_FAILURE_CAUSE_TOMBSTONE, ProjFS.prj_update_failure_causes, projectedfslib/PRJ_UPDATE_FAILURE_CAUSES, projectedfslib/PRJ_UPDATE_FAILURE_CAUSE_DIRTY_DATA, projectedfslib/PRJ_UPDATE_FAILURE_CAUSE_DIRTY_METADATA, projectedfslib/PRJ_UPDATE_FAILURE_CAUSE_NONE, projectedfslib/PRJ_UPDATE_FAILURE_CAUSE_READ_ONLY, projectedfslib/PRJ_UPDATE_FAILURE_CAUSE_TOMBSTONE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: projectedfslib.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - projectedfslib.h
api_name:
 - PRJ_UPDATE_FAILURE_CAUSES
product: Windows
targetos: Windows
req.typenames: PRJ_UPDATE_FAILURE_CAUSES
req.redist: 
---

# PRJ_UPDATE_FAILURE_CAUSES enumeration


## -description


Descriptions for the reason an update failed.


## -enum-fields




### -field PRJ_UPDATE_FAILURE_CAUSE_NONE

The update did not fail.


### -field PRJ_UPDATE_FAILURE_CAUSE_DIRTY_METADATA

The item was a dirty placeholder (hydrated or not), and the provider did not specify PRJ_UPDATE_ALLOW_DIRTY_METADATA in <a href="projfs.prj_update_types">PRJ_UPDATE_TYPES</a>.


### -field PRJ_UPDATE_FAILURE_CAUSE_DIRTY_DATA

The item was a full file and the provider did not specify PRJ_UPDATE_ALLOW_DIRTY_DATA in <a href="projfs.prj_update_types">PRJ_UPDATE_TYPES</a>.


### -field PRJ_UPDATE_FAILURE_CAUSE_TOMBSTONE

The item was a tombstone and the provider did not specify PRJ_UPDATE_ALLOW_TOMBSTONE in <a href="projfs.prj_update_types">PRJ_UPDATE_TYPES</a>.


### -field PRJ_UPDATE_FAILURE_CAUSE_READ_ONLY

The item had the DOS read-only bit set and the provider did not specify PRJ_UPDATE_ALLOW_READ_ONLY in <a href="projfs.prj_update_types">PRJ_UPDATE_TYPES</a>.

