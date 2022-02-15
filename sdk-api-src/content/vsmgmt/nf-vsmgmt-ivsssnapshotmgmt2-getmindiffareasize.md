---
UID: NF:vsmgmt.IVssSnapshotMgmt2.GetMinDiffAreaSize
title: IVssSnapshotMgmt2::GetMinDiffAreaSize (vsmgmt.h)
description: Returns the current minimum size of the shadow copy storage area.
helpviewer_keywords: ["GetMinDiffAreaSize","GetMinDiffAreaSize method [VSS]","GetMinDiffAreaSize method [VSS]","IVssSnapshotMgmt2 interface","IVssSnapshotMgmt2 interface [VSS]","GetMinDiffAreaSize method","IVssSnapshotMgmt2.GetMinDiffAreaSize","IVssSnapshotMgmt2::GetMinDiffAreaSize","base.ivsssnapshotmgmt2_getmindiffareasize","vsmgmt/IVssSnapshotMgmt2::GetMinDiffAreaSize"]
old-location: base\ivsssnapshotmgmt2_getmindiffareasize.htm
tech.root: base
ms.assetid: d1ee4499-07cb-4373-a3c9-892129a257db
ms.date: 12/05/2018
ms.keywords: GetMinDiffAreaSize, GetMinDiffAreaSize method [VSS], GetMinDiffAreaSize method [VSS],IVssSnapshotMgmt2 interface, IVssSnapshotMgmt2 interface [VSS],GetMinDiffAreaSize method, IVssSnapshotMgmt2.GetMinDiffAreaSize, IVssSnapshotMgmt2::GetMinDiffAreaSize, base.ivsssnapshotmgmt2_getmindiffareasize, vsmgmt/IVssSnapshotMgmt2::GetMinDiffAreaSize
req.header: vsmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVssSnapshotMgmt2::GetMinDiffAreaSize
 - vsmgmt/IVssSnapshotMgmt2::GetMinDiffAreaSize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VsMgmt.h
api_name:
 - IVssSnapshotMgmt2.GetMinDiffAreaSize
---

# IVssSnapshotMgmt2::GetMinDiffAreaSize


## -description

Returns the current minimum size of the shadow copy storage area.

## -parameters

### -param pllMinDiffAreaSize [out]

A pointer to a variable that receives the minimum size, in bytes, of the shadow copy storage area.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The shadow copy storage area minimum size is a per-computer setting that is specified by the <b>MinDiffAreaFileSize</b> registry key. For more information, see the entry for <b>MinDiffAreaFileSize</b> in <a href="/windows/desktop/Backup/registry-keys-for-backup-and-restore">Registry Keys and Values for Backup and Restore</a>.

## -see-also

<a href="/windows/desktop/api/vsmgmt/nn-vsmgmt-ivsssnapshotmgmt2">IVssSnapshotMgmt2</a>