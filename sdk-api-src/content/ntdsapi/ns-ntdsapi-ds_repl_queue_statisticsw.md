---
UID: NS:ntdsapi._DS_REPL_QUEUE_STATISTICSW
title: DS_REPL_QUEUE_STATISTICSW (ntdsapi.h)
description: Used to contain replication queue statistics.
helpviewer_keywords: ["DS_REPL_QUEUE_STATISTICSW","DS_REPL_QUEUE_STATISTICSW structure [Active Directory]","DS_REPL_QUEUE_STATISTICSW_BLOB","_DS_REPL_QUEUE_STATISTICSW","ad.ds_repl_queue_statisticsw","ntdsapi/DS_REPL_QUEUE_STATISTICSW"]
old-location: ad\ds_repl_queue_statisticsw.htm
tech.root: ad
ms.assetid: bfddd7ed-0ff4-46ca-84c2-39020acb37d0
ms.date: 12/05/2018
ms.keywords: DS_REPL_QUEUE_STATISTICSW, DS_REPL_QUEUE_STATISTICSW structure [Active Directory], DS_REPL_QUEUE_STATISTICSW_BLOB, _DS_REPL_QUEUE_STATISTICSW, ad.ds_repl_queue_statisticsw, ntdsapi/DS_REPL_QUEUE_STATISTICSW
req.header: ntdsapi.h
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
req.typenames: DS_REPL_QUEUE_STATISTICSW, DS_REPL_QUEUE_STATISTICSW_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DS_REPL_QUEUE_STATISTICSW
 - ntdsapi/_DS_REPL_QUEUE_STATISTICSW
 - DS_REPL_QUEUE_STATISTICSW
 - ntdsapi/DS_REPL_QUEUE_STATISTICSW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ntdsapi.h
api_name:
 - DS_REPL_QUEUE_STATISTICSW
---

# DS_REPL_QUEUE_STATISTICSW structure


## -description

The <b>DS_REPL_QUEUE_STATISTICSW</b> structure is used to contain replication queue statistics.

Reserved. Obtain this data using the <a href="/previous-versions/windows/desktop/legacy/ms676274(v=vs.85)">DS_REPL_QUEUE_STATISTICSW_BLOB</a> structure with the <a href="/previous-versions/windows/desktop/ldap/lightweight-directory-access-protocol-ldap-api">Lightweight Directory Access Protocol API</a> functions to obtain binary data for the <b>msDS-ReplQueueStatistics</b> attribute.

## -struct-fields

### -field ftimeCurrentOpStarted

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time that the currently running operation started.

### -field cNumPendingOps

Contains the number of currently pending operations.

### -field ftimeOldestSync

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time of the oldest synchronization operation.

### -field ftimeOldestAdd

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time of the oldest add operation.

### -field ftimeOldestMod

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time of the oldest modification operation.

### -field ftimeOldestDel

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time of the oldest delete operation.

### -field ftimeOldestUpdRefs

Contains a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure that contains the date and time of the oldest reference update operation.

## -remarks

<a href="/previous-versions/windows/desktop/legacy/ms676274(v=vs.85)">DS_REPL_QUEUE_STATISTICSW_BLOB</a> is an alias for this structure.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/ms676274(v=vs.85)">DS_REPL_QUEUE_STATISTICSW_BLOB</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>