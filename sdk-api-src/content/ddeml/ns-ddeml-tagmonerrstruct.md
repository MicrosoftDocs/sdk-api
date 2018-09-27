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



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648733(v=VS.85).aspx">MONCBSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648734(v=VS.85).aspx">MONCONVSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648736(v=VS.85).aspx">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648737(v=VS.85).aspx">MONLINKSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648738(v=VS.85).aspx">MONMSGSTRUCT</a>



<b>Reference</b>
 

 

