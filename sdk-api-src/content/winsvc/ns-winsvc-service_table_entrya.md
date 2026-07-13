---
UID: NS:winsvc._SERVICE_TABLE_ENTRYA
title: SERVICE_TABLE_ENTRYA (winsvc.h)
description: Specifies the ServiceMain function for a service that can run in the calling process. It is used by the StartServiceCtrlDispatcher function. (ANSI)
helpviewer_keywords: ["*LPSERVICE_TABLE_ENTRYA","LPSERVICE_TABLE_ENTRY","LPSERVICE_TABLE_ENTRY structure pointer","SERVICE_TABLE_ENTRY","SERVICE_TABLE_ENTRY structure","SERVICE_TABLE_ENTRYA","SERVICE_TABLE_ENTRYW","_win32_service_table_entry_str","base.service_table_entry_str","winsvc/LPSERVICE_TABLE_ENTRY","winsvc/SERVICE_TABLE_ENTRY","winsvc/SERVICE_TABLE_ENTRYA","winsvc/SERVICE_TABLE_ENTRYW"]
old-location: base\service_table_entry_str.htm
tech.root: security
ms.assetid: dd40c4f0-cbbe-429f-91c0-3ba141dab702
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_TABLE_ENTRYA, LPSERVICE_TABLE_ENTRY, LPSERVICE_TABLE_ENTRY structure pointer, SERVICE_TABLE_ENTRY, SERVICE_TABLE_ENTRY structure, SERVICE_TABLE_ENTRYA, SERVICE_TABLE_ENTRYW, _win32_service_table_entry_str, base.service_table_entry_str, winsvc/LPSERVICE_TABLE_ENTRY, winsvc/SERVICE_TABLE_ENTRY, winsvc/SERVICE_TABLE_ENTRYA, winsvc/SERVICE_TABLE_ENTRYW'
req.header: winsvc.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SERVICE_TABLE_ENTRYW (Unicode) and SERVICE_TABLE_ENTRYA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SERVICE_TABLE_ENTRYA, *LPSERVICE_TABLE_ENTRYA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SERVICE_TABLE_ENTRYA
 - winsvc/_SERVICE_TABLE_ENTRYA
 - LPSERVICE_TABLE_ENTRYA
 - winsvc/LPSERVICE_TABLE_ENTRYA
 - SERVICE_TABLE_ENTRYA
 - winsvc/SERVICE_TABLE_ENTRYA
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
 - SERVICE_TABLE_ENTRY
 - SERVICE_TABLE_ENTRYA
 - SERVICE_TABLE_ENTRYW
---

# SERVICE_TABLE_ENTRYA structure


## -description

Specifies the 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function for a service that can run in the calling process. It is used by the 
<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a> function.

## -struct-fields

### -field lpServiceName

The name of a service to be run in this service process.  

If the service is installed with the  SERVICE_WIN32_OWN_PROCESS service type, this member is ignored, but cannot be NULL. This member can be an empty string ("").

If the service is installed with the SERVICE_WIN32_SHARE_PROCESS service type, this member specifies the name of the service that uses the 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function pointed to by the <b>lpServiceProc</b> member.

### -field lpServiceProc

A pointer to a 
<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function.

## -see-also

<a href="/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>



<a href="/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a>

## -remarks

> [!NOTE]
> The winsvc.h header defines SERVICE_TABLE_ENTRY as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
