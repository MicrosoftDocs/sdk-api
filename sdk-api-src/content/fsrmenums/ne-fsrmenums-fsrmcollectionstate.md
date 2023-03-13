---
UID: NE:fsrmenums._FsrmCollectionState
title: FsrmCollectionState (fsrmenums.h)
description: Defines the possible states of a collection object.
helpviewer_keywords: ["FsrmCollectionState","FsrmCollectionState enumeration [File Server Resource Manager]","FsrmCollectionState_Cancelled","FsrmCollectionState_Committing","FsrmCollectionState_Complete","FsrmCollectionState_Fetching","fs.fsrmcollectionstate","fsrm.fsrmcollectionstate","fsrmenums/FsrmCollectionState","fsrmenums/FsrmCollectionState_Cancelled","fsrmenums/FsrmCollectionState_Committing","fsrmenums/FsrmCollectionState_Complete","fsrmenums/FsrmCollectionState_Fetching"]
old-location: fsrm\fsrmcollectionstate.htm
tech.root: fsrm
ms.assetid: 94d7cf83-7fa4-4fec-956d-f5b2e2c0bf68
ms.date: 12/05/2018
ms.keywords: FsrmCollectionState, FsrmCollectionState enumeration [File Server Resource Manager], FsrmCollectionState_Cancelled, FsrmCollectionState_Committing, FsrmCollectionState_Complete, FsrmCollectionState_Fetching, fs.fsrmcollectionstate, fsrm.fsrmcollectionstate, fsrmenums/FsrmCollectionState, fsrmenums/FsrmCollectionState_Cancelled, fsrmenums/FsrmCollectionState_Committing, fsrmenums/FsrmCollectionState_Complete, fsrmenums/FsrmCollectionState_Fetching
req.header: fsrmenums.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.typenames: FsrmCollectionState
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FsrmCollectionState
 - fsrmenums/_FsrmCollectionState
 - FsrmCollectionState
 - fsrmenums/FsrmCollectionState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FsrmEnums.h
api_name:
 - FsrmCollectionState
---

# FsrmCollectionState enumeration


## -description

Defines the possible states of a collection object.

## -enum-fields

### -field FsrmCollectionState_Fetching:1

The collection object is fetching data.

### -field FsrmCollectionState_Committing:2

The collection object is committing its data.

### -field FsrmCollectionState_Complete:3

The collection object is complete (has stopped fetching or committing data).

### -field FsrmCollectionState_Cancelled:4

The collection operation (fetching or committing) was canceled.

## -see-also

<a href="/previous-versions/windows/desktop/api/fsrm/nf-fsrm-ifsrmcollection-get_state">IFsrmCollection::State</a>
