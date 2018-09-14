---
UID: NS:ddeml.tagMONERRSTRUCT
title: tagMONERRSTRUCT
author: windows-sdk-content
description: Contains information about the current Dynamic Data Exchange (DDE) error. A DDE monitoring application can use this structure to monitor errors returned by DDE Management Library functions.
old-location: dataxchg\monerrstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monerrstruct.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PMONERRSTRUCT, MONERRSTRUCT, MONERRSTRUCT structure [Data Exchange], PMONERRSTRUCT, PMONERRSTRUCT structure pointer [Data Exchange], _win32_MONERRSTRUCT_str, _win32_monerrstruct_str_cpp, dataxchg.monerrstruct_str, ddeml/MONERRSTRUCT, ddeml/PMONERRSTRUCT, tagMONERRSTRUCT, winui._win32_monerrstruct_str"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddeml.h
api_name:
 - MONERRSTRUCT
product: Windows
targetos: Windows
req.typenames: MONERRSTRUCT, *PMONERRSTRUCT
req.redist: 
---

# tagMONERRSTRUCT structure


## -description


Contains information about the current Dynamic Data Exchange (DDE) error. A DDE monitoring application can use this structure to monitor errors returned by DDE Management Library functions. 


## -struct-fields




### -field cb

Type: <b>UINT</b>

The structure's size, in bytes. 


### -field wLastError

Type: <b>UINT</b>

The current error. 


### -field dwTime

Type: <b>DWORD</b>

The Windows time at which the error occurred. Windows time is the number of milliseconds that have elapsed since the system was booted. 


### -field hTask

Type: <b>HANDLE</b>

A handle to the task (application instance) that called the DDE function that caused the error. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/65bea5e0-ab86-4e00-9dbf-9809aab18616">MONCBSTRUCT</a>



<a href="https://msdn.microsoft.com/24fe9042-7b9f-4139-a9b5-d8c72529d897">MONCONVSTRUCT</a>



<a href="https://msdn.microsoft.com/d5c6b5f8-e999-4f79-bf7c-b7d74a3e9b46">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/db02a191-677b-4fae-88ec-c2b500249837">MONLINKSTRUCT</a>



<a href="https://msdn.microsoft.com/7d971b35-0c88-42c3-83b9-93d5de6c95f9">MONMSGSTRUCT</a>



<b>Reference</b>
 

 

