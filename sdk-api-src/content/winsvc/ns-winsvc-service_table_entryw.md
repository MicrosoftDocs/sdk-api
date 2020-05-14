---
UID: NS:winsvc._SERVICE_TABLE_ENTRYW
title: SERVICE_TABLE_ENTRYW (winsvc.h)
description: Specifies the ServiceMain function for a service that can run in the calling process. It is used by the StartServiceCtrlDispatcher function.helpviewer_keywords: ["*LPSERVICE_TABLE_ENTRYW","LPSERVICE_TABLE_ENTRY","LPSERVICE_TABLE_ENTRY structure pointer","SERVICE_TABLE_ENTRY","SERVICE_TABLE_ENTRY structure","SERVICE_TABLE_ENTRYA","SERVICE_TABLE_ENTRYW","_win32_service_table_entry_str","base.service_table_entry_str","winsvc/LPSERVICE_TABLE_ENTRY","winsvc/SERVICE_TABLE_ENTRY","winsvc/SERVICE_TABLE_ENTRYA","winsvc/SERVICE_TABLE_ENTRYW"]
old-location: base\service_table_entry_str.htm
tech.root: Services
ms.assetid: dd40c4f0-cbbe-429f-91c0-3ba141dab702
ms.date: 12/05/2018
ms.keywords: '*LPSERVICE_TABLE_ENTRYW, LPSERVICE_TABLE_ENTRY, LPSERVICE_TABLE_ENTRY structure pointer, SERVICE_TABLE_ENTRY, SERVICE_TABLE_ENTRY structure, SERVICE_TABLE_ENTRYA, SERVICE_TABLE_ENTRYW, _win32_service_table_entry_str, base.service_table_entry_str, winsvc/LPSERVICE_TABLE_ENTRY, winsvc/SERVICE_TABLE_ENTRY, winsvc/SERVICE_TABLE_ENTRYA, winsvc/SERVICE_TABLE_ENTRYW'
f1_keywords:
- winsvc/SERVICE_TABLE_ENTRY
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
req.unicode-ansi: SERVICE_TABLE_ENTRYW (Unicode) and SERVICE_TABLE_ENTRYA (ANSI)
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
- SERVICE_TABLE_ENTRY
- SERVICE_TABLE_ENTRYA
- SERVICE_TABLE_ENTRYW
targetos: Windows
req.typenames: SERVICE_TABLE_ENTRYW, *LPSERVICE_TABLE_ENTRYW
req.redist: 
ms.custom: 19H1
---

# SERVICE_TABLE_ENTRYW structure


## -description


Specifies the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function for a service that can run in the calling process. It is used by the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a> function.


## -struct-fields




### -field lpServiceName

The name of a service to be run in this service process.  

If the service is installed with the  SERVICE_WIN32_OWN_PROCESS service type, this member is ignored, but cannot be NULL. This member can be an empty string ("").

If the service is installed with the SERVICE_WIN32_SHARE_PROCESS service type, this member specifies the name of the service that uses the 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function pointed to by the <b>lpServiceProc</b> member.


### -field lpServiceProc

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a> function.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nc-winsvc-lpservice_main_functiona">ServiceMain</a>



<a href="https://docs.microsoft.com/windows/desktop/api/winsvc/nf-winsvc-startservicectrldispatchera">StartServiceCtrlDispatcher</a>
 

 

