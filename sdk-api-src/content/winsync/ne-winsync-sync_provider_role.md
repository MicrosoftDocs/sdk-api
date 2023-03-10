---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0001
title: SYNC_PROVIDER_ROLE (winsync.h)
description: Represents the role of a provider, relative to the other provider in the synchronization session.
helpviewer_keywords: ["SPR_DESTINATION","SPR_SOURCE","SYNC_PROVIDER_ROLE","SYNC_PROVIDER_ROLE enumeration [Windows Sync]","winsync.sync_provider_role","winsync/SPR_DESTINATION","winsync/SPR_SOURCE","winsync/SYNC_PROVIDER_ROLE"]
old-location: winsync\sync_provider_role.htm
tech.root: winsync
ms.assetid: 2409c8bf-c4fc-4986-8dde-cc11f0d52ed4
ms.date: 12/05/2018
ms.keywords: SPR_DESTINATION, SPR_SOURCE, SYNC_PROVIDER_ROLE, SYNC_PROVIDER_ROLE enumeration [Windows Sync], winsync.sync_provider_role, winsync/SPR_DESTINATION, winsync/SPR_SOURCE, winsync/SYNC_PROVIDER_ROLE
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
targetos: Windows
req.typenames: SYNC_PROVIDER_ROLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsync_0000_0000_0001
 - winsync/__MIDL___MIDL_itf_winsync_0000_0000_0001
 - SYNC_PROVIDER_ROLE
 - winsync/SYNC_PROVIDER_ROLE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsync.h
api_name:
 - SYNC_PROVIDER_ROLE
---

# SYNC_PROVIDER_ROLE enumeration


## -description

Represents the role of a provider, relative to the other provider in the synchronization session.

## -enum-fields

### -field SPR_SOURCE:0

The provider is the source provider.

### -field SPR_DESTINATION

The provider is the destination provider.

## -remarks

Changes flow from the source provider to the destination provider in a synchronization session.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-enumerations">Windows Sync Enumerations</a>
