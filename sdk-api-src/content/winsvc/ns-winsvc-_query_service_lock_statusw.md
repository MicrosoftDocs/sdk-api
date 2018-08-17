---
UID: NS:winsvc._QUERY_SERVICE_LOCK_STATUSW
title: "_QUERY_SERVICE_LOCK_STATUSW"
author: windows-sdk-content
description: Contains information about the lock status of a service control manager database. It is used by the QueryServiceLockStatus function.
old-location: base\query_service_lock_status_str.htm
old-project: services
ms.assetid: de9797b7-02b0-43cb-bed3-50b7e8676f36
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: "*LPQUERY_SERVICE_LOCK_STATUSW, LPQUERY_SERVICE_LOCK_STATUS, LPQUERY_SERVICE_LOCK_STATUS structure pointer, QUERY_SERVICE_LOCK_STATUS, QUERY_SERVICE_LOCK_STATUS structure, QUERY_SERVICE_LOCK_STATUSA, QUERY_SERVICE_LOCK_STATUSW, _QUERY_SERVICE_LOCK_STATUSW, _win32_query_service_lock_status_str, base.query_service_lock_status_str, winsvc/LPQUERY_SERVICE_LOCK_STATUS, winsvc/QUERY_SERVICE_LOCK_STATUS, winsvc/QUERY_SERVICE_LOCK_STATUSA, winsvc/QUERY_SERVICE_LOCK_STATUSW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winsvc.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: QUERY_SERVICE_LOCK_STATUSW, *LPQUERY_SERVICE_LOCK_STATUSW
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
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _QUERY_SERVICE_LOCK_STATUSW structure


## -description


Contains information about the lock status of a service control manager database. It is used by the 
<a href="https://msdn.microsoft.com/5139d31b-65f1-41ba-852a-91eab1dc366e">QueryServiceLockStatus</a> function.


## -struct-fields




### -field fIsLocked

The lock status of the database. If this member is nonzero, the database is locked. If it is zero, the database is unlocked.


### -field lpLockOwner

The name of the user who acquired the lock.


### -field dwLockDuration

The time since the lock was first acquired, in seconds.


## -see-also




<a href="https://msdn.microsoft.com/5139d31b-65f1-41ba-852a-91eab1dc366e">QueryServiceLockStatus</a>
 

 

