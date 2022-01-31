---
UID: NE:pla.__MIDL___MIDL_itf_pla_0001_0043_0007
title: CommitMode (pla.h)
description: Defines the action to take when committing changes to the data collector set.
helpviewer_keywords: ["CommitMode","CommitMode enumeration [PLA]","base.commitmode","pla.commitmode","pla/CommitMode","pla/plaCreateNew","pla/plaCreateOrModify","pla/plaFlushTrace","pla/plaModify","pla/plaUpdateRunningInstance","pla/plaValidateOnly","plaCreateNew","plaCreateOrModify","plaFlushTrace","plaModify","plaUpdateRunningInstance","plaValidateOnly"]
old-location: pla\commitmode.htm
tech.root: PLA
ms.assetid: 3c485b4d-ba0b-456a-b942-27829371d7fb
ms.date: 12/05/2018
ms.keywords: CommitMode, CommitMode enumeration [PLA], base.commitmode, pla.commitmode, pla/CommitMode, pla/plaCreateNew, pla/plaCreateOrModify, pla/plaFlushTrace, pla/plaModify, pla/plaUpdateRunningInstance, pla/plaValidateOnly, plaCreateNew, plaCreateOrModify, plaFlushTrace, plaModify, plaUpdateRunningInstance, plaValidateOnly
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: CommitMode
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_pla_0001_0043_0007
 - pla/__MIDL___MIDL_itf_pla_0001_0043_0007
 - CommitMode
 - pla/CommitMode
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pla.h
api_name:
 - CommitMode
---

# CommitMode enumeration


## -description

Defines the action to take when committing changes to the data collector set.

## -enum-fields

### -field plaCreateNew:0x1

Save the set. The set must not already exist. 

The set is not saved if it is a trace session.

### -field plaModify:0x2

Update a previously saved set.

### -field plaCreateOrModify:0x3

Save the set. If the set already exists, update the set.

The set is not saved if it is a trace session.

### -field plaUpdateRunningInstance:0x10

Apply the updated property values to the currently running data set.

### -field plaFlushTrace:0x20

Flush the buffers for an Event Tracing for Windows trace session. This action applies only to sets that contain trace data collectors.

### -field plaValidateOnly:0x1000

Perform validation only on the set.

## -remarks

All commit modes validate the set.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a>
