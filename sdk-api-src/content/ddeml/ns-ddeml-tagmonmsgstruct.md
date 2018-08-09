---
UID: NS:ddeml.tagMONMSGSTRUCT
title: tagMONMSGSTRUCT
author: windows-sdk-content
description: Contains information about a Dynamic Data Exchange (DDE) message. A DDE monitoring application can use this structure to obtain information about a DDE message that was sent or posted.
old-location: dataxchg\monmsgstruct_str.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monmsgstruct.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMONMSGSTRUCT, MONMSGSTRUCT, MONMSGSTRUCT structure [Data Exchange], PMONMSGSTRUCT, PMONMSGSTRUCT structure pointer [Data Exchange], _win32_MONMSGSTRUCT_str, _win32_monmsgstruct_str_cpp, dataxchg.monmsgstruct_str, ddeml/MONMSGSTRUCT, ddeml/PMONMSGSTRUCT, tagMONMSGSTRUCT, winui._win32_monmsgstruct_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddeml.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MONMSGSTRUCT, *PMONMSGSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddeml.h
api_name:
 - MONMSGSTRUCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagMONMSGSTRUCT structure


## -description


Contains information about a Dynamic Data Exchange (DDE) message. A DDE monitoring application can use this structure to obtain information about a DDE message that was sent or posted. 


## -struct-fields




### -field cb

Type: <b>UINT</b>

The structure's size, in bytes. 


### -field hwndTo

Type: <b>HWND</b>

A handle to the window that receives the DDE message. 


### -field dwTime

Type: <b>DWORD</b>

The Windows time at which the message was sent or posted. Windows time is the number of milliseconds that have elapsed since the system was booted. 


### -field hTask

Type: <b>HANDLE</b>

A handle to the task (application instance) containing the window that receives the DDE message. 


### -field wMsg

Type: <b>UINT</b>

The identifier of the DDE message. 


### -field wParam

Type: <b>WPARAM</b>

The <b>wParam</b> parameter of the DDE message. 


### -field lParam

Type: <b>LPARAM</b>

The <b>lParam</b> parameter of the DDE message. 


### -field dmhd

Type: <b><a href="https://msdn.microsoft.com/d556c210-8a4a-4e43-a596-3350a89609fe">DDEML_MSG_HOOK_DATA</a></b>

Additional information about the DDE message. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d556c210-8a4a-4e43-a596-3350a89609fe">DDEML_MSG_HOOK_DATA</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/65bea5e0-ab86-4e00-9dbf-9809aab18616">MONCBSTRUCT</a>



<a href="https://msdn.microsoft.com/24fe9042-7b9f-4139-a9b5-d8c72529d897">MONCONVSTRUCT</a>



<a href="https://msdn.microsoft.com/4e7647a0-c41e-4ec9-b441-01538e83aca3">MONERRSTRUCT</a>



<a href="https://msdn.microsoft.com/d5c6b5f8-e999-4f79-bf7c-b7d74a3e9b46">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/db02a191-677b-4fae-88ec-c2b500249837">MONLINKSTRUCT</a>



<b>Reference</b>
 

 

