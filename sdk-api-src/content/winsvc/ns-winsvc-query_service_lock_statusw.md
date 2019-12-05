---
UID: NS:winsvc._QUERY_SERVICE_LOCK_STATUSW
title: QUERY_SERVICE_LOCK_STATUSW (winsvc.h)
description: Contains information about the lock status of a service control manager database. It is used by the QueryServiceLockStatus function.
old-location: base\query_service_lock_status_str.htm
tech.root: Services
ms.assetid: de9797b7-02b0-43cb-bed3-50b7e8676f36
ms.date: 12/05/2018
ms.keywords: '*LPQUERY_SERVICE_LOCK_STATUSW, LPQUERY_SERVICE_LOCK_STATUS, LPQUERY_SERVICE_LOCK_STATUS structure pointer, QUERY_SERVICE_LOCK_STATUS, QUERY_SERVICE_LOCK_STATUS structure, QUERY_SERVICE_LOCK_STATUSA, QUERY_SERVICE_LOCK_STATUSW, _win32_query_service_lock_status_str, base.query_service_lock_status_str, winsvc/LPQUERY_SERVICE_LOCK_STATUS, winsvc/QUERY_SERVICE_LOCK_STATUS, winsvc/QUERY_SERVICE_LOCK_STATUSA, winsvc/QUERY_SERVICE_LOCK_STATUSW'
ms.topic: struct
f1_keywords:
- winsvc/QUERY_SERVICE_LOCK_STATUS
dev_langs:
- c++
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QUERY_SERVICE_LOCK_STATUSW (Unicode) and QUERY_SERVICE_LOCK_STATUSA (ANSI)
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
- Winsvc.h
api_name:
- QUERY_SERVICE_LOCK_STATUS
- QUERY_SERVICE_LOCK_STATUSA
- QUERY_SERVICE_LOCK_STATUSW
targetos: Windows
req.typenames: QUERY_SERVICE_LOCK_STATUSW, *LPQUERY_SERVICE_LOCK_STATUSW
req.redist: 
ms.custom: 19H1
---

# QUERY_SERVICE_LOCK_STATUSW structure


## -description


Contains information about the lock status of a service control manager database. It is used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-queryservicelockstatusa">QueryServiceLockStatus</a> function.


## -struct-fields




### -field fIsLocked

The lock status of the database. If this member is nonzero, the database is locked. If it is zero, the database is unlocked.


### -field lpLockOwner

The name of the user who acquired the lock.


### -field dwLockDuration

The time since the lock was first acquired, in seconds.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-queryservicelockstatusa">QueryServiceLockStatus</a>
 

 

