---
UID: NE:winsync.__MIDL___MIDL_itf_winsync_0000_0000_0007
title: SYNC_SERIALIZATION_VERSION (winsync.h)
description: Represents the version of Microsoft Sync Framework that a particular component is compatible with.
helpviewer_keywords: ["SYNC_SERIALIZATION_VERSION","SYNC_SERIALIZATION_VERSION enumeration [Windows Sync]","SYNC_SERIALIZATION_VERSION_V1","SYNC_SERIALIZATION_VERSION_V2","winsync.sync_serialization_version","winsync/SYNC_SERIALIZATION_VERSION","winsync/SYNC_SERIALIZATION_VERSION_V1","winsync/SYNC_SERIALIZATION_VERSION_V2"]
old-location: winsync\sync_serialization_version.htm
tech.root: winsync
ms.assetid: 840a1f5e-56f7-4774-a154-0dab66c3d407
ms.date: 12/05/2018
ms.keywords: SYNC_SERIALIZATION_VERSION, SYNC_SERIALIZATION_VERSION enumeration [Windows Sync], SYNC_SERIALIZATION_VERSION_V1, SYNC_SERIALIZATION_VERSION_V2, winsync.sync_serialization_version, winsync/SYNC_SERIALIZATION_VERSION, winsync/SYNC_SERIALIZATION_VERSION_V1, winsync/SYNC_SERIALIZATION_VERSION_V2
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
req.typenames: SYNC_SERIALIZATION_VERSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_winsync_0000_0000_0007
 - winsync/__MIDL___MIDL_itf_winsync_0000_0000_0007
 - SYNC_SERIALIZATION_VERSION
 - winsync/SYNC_SERIALIZATION_VERSION
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
 - SYNC_SERIALIZATION_VERSION
---

# SYNC_SERIALIZATION_VERSION enumeration


## -description

Represents the version of <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a> that a particular component is compatible with. For an overview of what is involved in building synchronization providers using  <a href="https://www.microsoft.com/downloads/details.aspx?familyid=A3EE7BC5-A823-4FB4-B152-9E8CE9D5546F&displaylang=en">Microsoft Sync Framework</a>, see <a href="/previous-versions/windows/desktop/winsync/options-for-building-a-synchronization-provider">Options for Building a Synchronization Provider</a>.

## -enum-fields

### -field SYNC_SERIALIZATION_VERSION_V1:1

Indicates a component is compatible with Sync Framework 1.0.

### -field SYNC_SERIALIZATION_VERSION_V2:4

Indicates a component is compatible with Sync Framework 2.0.

### -field SYNC_SERIALIZATION_VERSION_V3:5

## -remarks

A component that is designed to work with a particular version of Sync Framework can indicate the version for which it is designed. This way, when Sync Framework changes in later versions, a component designed for an earlier version will continue to function as expected.

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-enumerations">Windows Sync Enumerations</a>
