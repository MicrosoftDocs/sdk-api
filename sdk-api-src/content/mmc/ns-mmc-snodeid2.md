---
UID: NS:mmc._SNodeID2
title: SNodeID2 (mmc.h)
description: The SNodeID2 structure is introduced in MMC 1.2, and replaces the SNodeID structure.
helpviewer_keywords: ["SNodeID2","SNodeID2 structure [MMC]","_slate_snodeid2","mmc.snodeid2","mmc/SNodeID2"]
old-location: mmc\snodeid2.htm
tech.root: mmc
ms.assetid: d7a0a5db-a84f-48f3-b1fb-5bccb104b62a
ms.date: 12/05/2018
ms.keywords: SNodeID2, SNodeID2 structure [MMC], _slate_snodeid2, mmc.snodeid2, mmc/SNodeID2
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: SNodeID2
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SNodeID2
 - mmc/_SNodeID2
 - SNodeID2
 - mmc/SNodeID2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - SNodeID2
---

# SNodeID2 structure


## -description

The 
<b>SNodeID2</b> structure is introduced in MMC 1.2, and replaces the 
<a href="/windows/desktop/api/mmc/ns-mmc-snodeid">SNodeID</a> structure.

The 
<b>SNodeID2</b> structure is used by the 
<a href="/previous-versions/windows/desktop/mmc/ccf-nodeid2">CCF_NODEID2</a> clipboard format.

The 
<b>SNodeID2</b> structure contains an array of bytes that represent the node ID.

## -struct-fields

### -field dwFlags

Currently, only the MMC_NODEID_SLOW_RETRIEVAL flag is defined for <b>dwFlags</b>. If this flag is set, MMC will not persist the specified scope item except where absolutely necessary, as for example for console taskpads. Console taskpads always persist the target items and task target items.

### -field cBytes

The count of bytes in the <b>id</b> array.

### -field id

The bytes that contains the node ID of the scope item.

## -remarks

For details on using the 
<b>SNodeID2</b> structure with the CCF_NODEID2 clipboard format, see 
<a href="/previous-versions/windows/desktop/mmc/ccf-nodeid2">CCF_NODEID2</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-nodeid2">CCF_NODEID2</a>