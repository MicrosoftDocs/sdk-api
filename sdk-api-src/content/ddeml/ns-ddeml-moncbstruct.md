---
UID: NS:ddeml.tagMONCBSTRUCT
title: MONCBSTRUCT (ddeml.h)
description: Contains information about the current Dynamic Data Exchange (DDE) transaction. A DDE debugging application can use this structure when monitoring transactions that the system passes to the DDE callback functions of other applications.
helpviewer_keywords: ["*PMONCBSTRUCT","MONCBSTRUCT","MONCBSTRUCT structure [Data Exchange]","PMONCBSTRUCT","PMONCBSTRUCT structure pointer [Data Exchange]","_win32_MONCBSTRUCT_str","_win32_moncbstruct_str_cpp","dataxchg.moncbstruct_str","ddeml/MONCBSTRUCT","ddeml/PMONCBSTRUCT","winui._win32_moncbstruct_str"]
old-location: dataxchg\moncbstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\moncbstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PMONCBSTRUCT, MONCBSTRUCT, MONCBSTRUCT structure [Data Exchange], PMONCBSTRUCT, PMONCBSTRUCT structure pointer [Data Exchange], _win32_MONCBSTRUCT_str, _win32_moncbstruct_str_cpp, dataxchg.moncbstruct_str, ddeml/MONCBSTRUCT, ddeml/PMONCBSTRUCT, winui._win32_moncbstruct_str'
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
req.typenames: MONCBSTRUCT, *PMONCBSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMONCBSTRUCT
 - ddeml/tagMONCBSTRUCT
 - PMONCBSTRUCT
 - ddeml/PMONCBSTRUCT
 - MONCBSTRUCT
 - ddeml/MONCBSTRUCT
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
 - MONCBSTRUCT
---

# MONCBSTRUCT structure


## -description

Contains information about the current Dynamic Data Exchange (DDE) transaction. A DDE debugging application can use this structure when monitoring transactions that the system passes to the DDE callback functions of other applications.

## -struct-fields

### -field cb

Type: <b>UINT</b>

The structure's size, in bytes.

### -field dwTime

Type: <b>DWORD</b>

The Windows time at which the transaction occurred. Windows time is the number of milliseconds that have elapsed since the system was booted.

### -field hTask

Type: <b>HANDLE</b>

A handle to the task (application instance) containing the DDE callback function that received the transaction.

### -field dwRet

Type: <b>DWORD</b>

The value returned by the DDE callback function that processed the transaction.

### -field wType

Type: <b>UINT</b>

The transaction type.

### -field wFmt

Type: <b>UINT</b>

The format of the data exchanged (if any) during the transaction.

### -field hConv

Type: <b>HCONV</b>

A handle to the conversation in which the transaction took place.

### -field hsz1

Type: <b>HSZ</b>

A handle to a string.

### -field hsz2

Type: <b>HSZ</b>

A handle to a string.

### -field hData

Type: <b>HDDEDATA</b>

A handle to the data exchanged (if any) during the transaction.

### -field dwData1

Type: <b>ULONG_PTR</b>

Additional data.

### -field dwData2

Type: <b>ULONG_PTR</b>

Additional data.

### -field cc

Type: <b><a href="/windows/desktop/api/ddeml/ns-ddeml-convcontext">CONVCONTEXT</a></b>

The language information used to share data in different languages.

### -field cbData

Type: <b>DWORD</b>

The amount, in bytes, of data being passed with the transaction. This value can be more than 32 bytes.

### -field Data

Type: <b>DWORD[8]</b>

Contains the first 32 bytes of data being passed with the transaction (<code>8 * sizeof(DWORD)</code>).

## -see-also

<a href="/windows/desktop/api/ddeml/ns-ddeml-convcontext">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monerrstruct">MONERRSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monhszstructa">MONHSZSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monlinkstruct">MONLINKSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monmsgstruct">MONMSGSTRUCT</a>



<b>Reference</b>