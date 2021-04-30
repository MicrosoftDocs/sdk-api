---
UID: NS:ddeml.tagMONERRSTRUCT
title: MONERRSTRUCT (ddeml.h)
description: Contains information about the current Dynamic Data Exchange (DDE) error. A DDE monitoring application can use this structure to monitor errors returned by DDE Management Library functions.
helpviewer_keywords: ["*PMONERRSTRUCT","MONERRSTRUCT","MONERRSTRUCT structure [Data Exchange]","PMONERRSTRUCT","PMONERRSTRUCT structure pointer [Data Exchange]","_win32_MONERRSTRUCT_str","_win32_monerrstruct_str_cpp","dataxchg.monerrstruct_str","ddeml/MONERRSTRUCT","ddeml/PMONERRSTRUCT","winui._win32_monerrstruct_str"]
old-location: dataxchg\monerrstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monerrstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PMONERRSTRUCT, MONERRSTRUCT, MONERRSTRUCT structure [Data Exchange], PMONERRSTRUCT, PMONERRSTRUCT structure pointer [Data Exchange], _win32_MONERRSTRUCT_str, _win32_monerrstruct_str_cpp, dataxchg.monerrstruct_str, ddeml/MONERRSTRUCT, ddeml/PMONERRSTRUCT, winui._win32_monerrstruct_str'
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
targetos: Windows
req.typenames: MONERRSTRUCT, *PMONERRSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMONERRSTRUCT
 - ddeml/tagMONERRSTRUCT
 - PMONERRSTRUCT
 - ddeml/PMONERRSTRUCT
 - MONERRSTRUCT
 - ddeml/MONERRSTRUCT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddeml.h
api_name:
 - MONERRSTRUCT
---

# MONERRSTRUCT structure


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



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-moncbstruct">MONCBSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monconvstruct">MONCONVSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monhszstructa">MONHSZSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monlinkstruct">MONLINKSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monmsgstruct">MONMSGSTRUCT</a>



<b>Reference</b>