---
UID: NE:cfapi.CF_IN_SYNC_STATE
title: CF_IN_SYNC_STATE (cfapi.h)
author: windows-sdk-content
description: Specifies the in-sync state for placeholder files and folders.
old-location: cloudapi\cf_in_sync_state.htm
tech.root: cfApi
ms.assetid: 05F99E47-00EE-422C-BDDF-CCCDDD4DADED
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CF_IN_SYNC_STATE, CF_IN_SYNC_STATE enumeration, CF_IN_SYNC_STATE_IN_SYNC, CF_IN_SYNC_STATE_NOT_IN_SYNC, cfapi/CF_IN_SYNC_STATE, cfapi/CF_IN_SYNC_STATE_IN_SYNC, cfapi/CF_IN_SYNC_STATE_NOT_IN_SYNC, cloudApi.cf_in_sync_state
ms.topic: enum
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - CfApi.h
api_name:
 - CF_IN_SYNC_STATE
product: Windows
targetos: Windows
req.typenames: CF_IN_SYNC_STATE
req.redist: 
---

# CF_IN_SYNC_STATE enumeration


## -description


Specifies the in-sync state for placeholder files and folders.


## -enum-fields




### -field CF_IN_SYNC_STATE_NOT_IN_SYNC

The platform clears the placeholder’s in-sync state upon a successful return from the <a href="https://msdn.microsoft.com/1CB7955D-E530-4F34-8D67-BC608F8B6AF1">CfSetInSyncState</a> call.


### -field CF_IN_SYNC_STATE_IN_SYNC

The platform sets the placeholder’s in-sync state upon a successful return from the <a href="https://msdn.microsoft.com/1CB7955D-E530-4F34-8D67-BC608F8B6AF1">CfSetInSyncState</a> call.

