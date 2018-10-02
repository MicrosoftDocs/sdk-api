---
UID: NS:winsvc._SERVICE_TABLE_ENTRYA
title: "_SERVICE_TABLE_ENTRYA"
author: windows-sdk-content
description: Specifies the ServiceMain function for a service that can run in the calling process. It is used by the StartServiceCtrlDispatcher function.
old-location: base\service_table_entry_str.htm
tech.root: Services
ms.assetid: dd40c4f0-cbbe-429f-91c0-3ba141dab702
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*LPSERVICE_TABLE_ENTRYA, LPSERVICE_TABLE_ENTRY, LPSERVICE_TABLE_ENTRY structure pointer, SERVICE_TABLE_ENTRY, SERVICE_TABLE_ENTRY structure, SERVICE_TABLE_ENTRYA, SERVICE_TABLE_ENTRYW, _SERVICE_TABLE_ENTRYA, _win32_service_table_entry_str, base.service_table_entry_str, winsvc/LPSERVICE_TABLE_ENTRY, winsvc/SERVICE_TABLE_ENTRY, winsvc/SERVICE_TABLE_ENTRYA, winsvc/SERVICE_TABLE_ENTRYW"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: SERVICE_TABLE_ENTRYA, *LPSERVICE_TABLE_ENTRYA
req.redist: 
---

# _SERVICE_TABLE_ENTRYA structure


## -description


Specifies the 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function for a service that can run in the calling process. It is used by the 
<a href="https://msdn.microsoft.com/8e275eb7-a8af-4bd7-bb39-0eac4f3735ad">StartServiceCtrlDispatcher</a> function.


## -struct-fields




### -field lpServiceName

The name of a service to be run in this service process.  

If the service is installed with the  SERVICE_WIN32_OWN_PROCESS service type, this member is ignored, but cannot be NULL. This member can be an empty string ("").

If the service is installed with the SERVICE_WIN32_SHARE_PROCESS service type, this member specifies the name of the service that uses the 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function pointed to by the <b>lpServiceProc</b> member.


### -field lpServiceProc

A pointer to a 
<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a> function.


## -see-also




<a href="https://msdn.microsoft.com/d7f3235e-91bd-4107-a30c-4a8f9a6c731e">ServiceMain</a>



<a href="https://msdn.microsoft.com/8e275eb7-a8af-4bd7-bb39-0eac4f3735ad">StartServiceCtrlDispatcher</a>
 

 

