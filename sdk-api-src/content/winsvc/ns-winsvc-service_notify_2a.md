---
UID: NS:winsvc._SERVICE_NOTIFY_2A
title: SERVICE_NOTIFY_2A (winsvc.h)
description: Represents service status notification information. (ANSI)
helpviewer_keywords: ["*PSERVICE_NOTIFYA","*PSERVICE_NOTIFY_2A","PSERVICE_NOTIFY","PSERVICE_NOTIFY structure pointer","SERVICE_NOTIFY","SERVICE_NOTIFY structure","SERVICE_NOTIFYA","SERVICE_NOTIFYW","SERVICE_NOTIFY_2","SERVICE_NOTIFY_2A","base.service_notify","winsvc/PSERVICE_NOTIFY","winsvc/SERVICE_NOTIFY","winsvc/SERVICE_NOTIFYA","winsvc/SERVICE_NOTIFYW"]
old-location: base\service_notify.htm
tech.root: security
ms.assetid: 52ede72e-eb50-48e2-b5c1-125816f6fe57
ms.date: 12/05/2018
ms.keywords: '*PSERVICE_NOTIFYA, *PSERVICE_NOTIFY_2A, PSERVICE_NOTIFY, PSERVICE_NOTIFY structure pointer, SERVICE_NOTIFY, SERVICE_NOTIFY structure, SERVICE_NOTIFYA, SERVICE_NOTIFYW, SERVICE_NOTIFY_2, SERVICE_NOTIFY_2A, base.service_notify, winsvc/PSERVICE_NOTIFY, winsvc/SERVICE_NOTIFY, winsvc/SERVICE_NOTIFYA, winsvc/SERVICE_NOTIFYW'
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SERVICE_NOTIFYW (Unicode) and SERVICE_NOTIFYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_NOTIFY_2A, *PSERVICE_NOTIFY_2A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_NOTIFY_2A
 - winsvc/_SERVICE_NOTIFY_2A
 - PSERVICE_NOTIFY_2A
 - winsvc/PSERVICE_NOTIFY_2A
 - SERVICE_NOTIFY_2A
 - winsvc/SERVICE_NOTIFY_2A
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
 - SERVICE_NOTIFY
 - SERVICE_NOTIFYA
 - SERVICE_NOTIFYW
---

# SERVICE_NOTIFY_2A structure


## -description

Represents service status notification information. It is used by the <a href="/windows/desktop/api/winsvc/nf-winsvc-notifyservicestatuschangea">NotifyServiceStatusChange</a> function.

## -struct-fields

### -field dwVersion

The structure version. This member must be <b>SERVICE_NOTIFY_STATUS_CHANGE</b> (2).

### -field pfnNotifyCallback

A pointer to the callback function. For more information, see Remarks.

### -field pContext

Any user-defined data to be passed to the callback function.

### -field dwNotificationStatus

A value that indicates the notification status. If this member is <b>ERROR_SUCCESS</b>, the notification has succeeded and the <b>ServiceStatus</b> member contains valid information. If this member is <b>ERROR_SERVICE_MARKED_FOR_DELETE</b>, the service has been marked for deletion and the service handle used by <a href="/windows/desktop/api/winsvc/nf-winsvc-notifyservicestatuschangea">NotifyServiceStatusChange</a> must be closed.

### -field ServiceStatus

A <a href="/windows/desktop/api/winsvc/ns-winsvc-service_status_process">SERVICE_STATUS_PROCESS</a> structure that contains the service status information. This member is only valid if <b>dwNotificationStatus</b> is <b>ERROR_SUCCESS</b>.

### -field dwNotificationTriggered

If <b>dwNotificationStatus</b> is <b>ERROR_SUCCESS</b>, this member contains a bitmask of the notifications that triggered this call to the callback function.

### -field pszServiceNames

If <b>dwNotificationStatus</b> is <b>ERROR_SUCCESS</b> and the notification is <b>SERVICE_NOTIFY_CREATED</b> or <b>SERVICE_NOTIFY_DELETED</b>, this member is valid and it is a <b>MULTI_SZ</b> string that contains one or more service names. The names of the created services will have a '/' prefix so you can distinguish them from the names of the deleted services.

If this member is valid, the notification callback function must free the string using the <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a> function.

## -remarks

The callback function is declared as follows:


``` syntax
typedef VOID( CALLBACK * PFN_SC_NOTIFY_CALLBACK ) (
    IN PVOID pParameter 
);
```

The callback function receives a pointer to the <b>SERVICE_NOTIFY</b> structure provided by the caller.





> [!NOTE]
> The winsvc.h header defines SERVICE_NOTIFY_2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/winsvc/nf-winsvc-notifyservicestatuschangea">NotifyServiceStatusChange</a>



<a href="/windows/desktop/api/winsvc/ns-winsvc-service_status_process">SERVICE_STATUS_PROCESS</a>
