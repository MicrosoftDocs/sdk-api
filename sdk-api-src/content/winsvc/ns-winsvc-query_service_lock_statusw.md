---
UID: NS:winsvc._QUERY_SERVICE_LOCK_STATUSW
title: QUERY_SERVICE_LOCK_STATUSW (winsvc.h)
description: Contains information about the lock status of a service control manager database. It is used by the QueryServiceLockStatus function. (Unicode)
helpviewer_keywords: ["*LPQUERY_SERVICE_LOCK_STATUSW","LPQUERY_SERVICE_LOCK_STATUS","LPQUERY_SERVICE_LOCK_STATUS structure pointer","QUERY_SERVICE_LOCK_STATUS","QUERY_SERVICE_LOCK_STATUS structure","QUERY_SERVICE_LOCK_STATUSA","QUERY_SERVICE_LOCK_STATUSW","_win32_query_service_lock_status_str","base.query_service_lock_status_str","winsvc/LPQUERY_SERVICE_LOCK_STATUS","winsvc/QUERY_SERVICE_LOCK_STATUS","winsvc/QUERY_SERVICE_LOCK_STATUSA","winsvc/QUERY_SERVICE_LOCK_STATUSW"]
old-location: base\query_service_lock_status_str.htm
tech.root: security
ms.assetid: de9797b7-02b0-43cb-bed3-50b7e8676f36
ms.date: 12/05/2018
ms.keywords: '*LPQUERY_SERVICE_LOCK_STATUSW, LPQUERY_SERVICE_LOCK_STATUS, LPQUERY_SERVICE_LOCK_STATUS structure pointer, QUERY_SERVICE_LOCK_STATUS, QUERY_SERVICE_LOCK_STATUS structure, QUERY_SERVICE_LOCK_STATUSA, QUERY_SERVICE_LOCK_STATUSW, _win32_query_service_lock_status_str, base.query_service_lock_status_str, winsvc/LPQUERY_SERVICE_LOCK_STATUS, winsvc/QUERY_SERVICE_LOCK_STATUS, winsvc/QUERY_SERVICE_LOCK_STATUSA, winsvc/QUERY_SERVICE_LOCK_STATUSW'
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
targetos: Windows
req.typenames: QUERY_SERVICE_LOCK_STATUSW, *LPQUERY_SERVICE_LOCK_STATUSW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _QUERY_SERVICE_LOCK_STATUSW
 - winsvc/_QUERY_SERVICE_LOCK_STATUSW
 - LPQUERY_SERVICE_LOCK_STATUSW
 - winsvc/LPQUERY_SERVICE_LOCK_STATUSW
 - QUERY_SERVICE_LOCK_STATUSW
 - winsvc/QUERY_SERVICE_LOCK_STATUSW
dev_langs:
 - c++
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
---

# QUERY_SERVICE_LOCK_STATUSW structure


## -description

Contains information about the lock status of a service control manager database. It is used by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicelockstatusa">QueryServiceLockStatus</a> function.

## -struct-fields

### -field fIsLocked

The lock status of the database. If this member is nonzero, the database is locked. If it is zero, the database is unlocked.

### -field lpLockOwner

The name of the user who acquired the lock.

### -field dwLockDuration

The time since the lock was first acquired, in seconds.

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-queryservicelockstatusa">QueryServiceLockStatus</a>

## -remarks

> [!NOTE]
> The winsvc.h header defines QUERY_SERVICE_LOCK_STATUS as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
