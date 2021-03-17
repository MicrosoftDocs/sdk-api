---
UID: NS:mmc._SNodeID
title: SNodeID (mmc.h)
description: The SNodeID structure is introduced in MMC 1.1, and is replaced by the SNodeID2 structure in MMC 1.2.
helpviewer_keywords: ["SNodeID","SNodeID structure [MMC]","_slate_snodeid","mmc.snodeid","mmc/SNodeID"]
old-location: mmc\snodeid.htm
tech.root: mmc
ms.assetid: aeaee0d8-7abf-4549-b184-326ab130fcb7
ms.date: 12/05/2018
ms.keywords: SNodeID, SNodeID structure [MMC], _slate_snodeid, mmc.snodeid, mmc/SNodeID
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
req.typenames: SNodeID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SNodeID
 - mmc/_SNodeID
 - SNodeID
 - mmc/SNodeID
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
 - SNodeID
---

# SNodeID structure


## -description

The 
<b>SNodeID</b> structure is introduced in MMC 1.1, and is replaced by the 
<a href="/windows/desktop/api/mmc/ns-mmc-snodeid2">SNodeID2</a> structure in MMC 1.2.

The 
<b>SNodeID</b> structure defines the format of the data for the 
<a href="/previous-versions/windows/desktop/mmc/ccf-nodeid">CCF_NODEID</a> clipboard format.

The 
<b>SNodeID</b> structure contains an array of bytes that represent the node ID.

## -struct-fields

### -field cBytes

The count of bytes in the <b>id</b> array.

The snap-in can also specify that a scope item should not be re-expanded when the console is reopened. To do this, set the <b>cBytes</b> member to 0 (zero) and return <b>S_OK</b> in the <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> method. Be aware that this setting not only keeps the selected item from being persisted but also prevents its parent item from automatically expanding when the console file is reopened.

### -field id

The bytes that contains the node ID of the scope item.

## -remarks

Your snap-in should support the <b>CCF_NODEID</b> clipboard format in its <a href="/windows/desktop/api/objidl/nf-objidl-idataobject-getdata">IDataObject::GetData</a> method if any of its enumerated items has a volatile display name (such as the current computer name) or if any enumerated items should not be restored when the console file is reopened.

For details on using the 
<b>SNodeID</b> structure and <b>CCF_NODEID</b> clipboard format, see 
<a href="/previous-versions/windows/desktop/mmc/ccf-nodeid">CCF_NODEID</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-nodeid">CCF_NODEID</a>