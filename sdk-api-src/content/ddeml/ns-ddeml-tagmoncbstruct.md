---
UID: NS:ddeml.tagMONCBSTRUCT
title: tagMONCBSTRUCT
author: windows-sdk-content
description: Contains information about the current Dynamic Data Exchange (DDE) transaction. A DDE debugging application can use this structure when monitoring transactions that the system passes to the DDE callback functions of other applications.
old-location: dataxchg\moncbstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\moncbstruct.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PMONCBSTRUCT, MONCBSTRUCT, MONCBSTRUCT structure [Data Exchange], PMONCBSTRUCT, PMONCBSTRUCT structure pointer [Data Exchange], _win32_MONCBSTRUCT_str, _win32_moncbstruct_str_cpp, dataxchg.moncbstruct_str, ddeml/MONCBSTRUCT, ddeml/PMONCBSTRUCT, tagMONCBSTRUCT, winui._win32_moncbstruct_str"
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
 - MONCBSTRUCT
product: Windows
targetos: Windows
req.typenames: MONCBSTRUCT, *PMONCBSTRUCT
req.redist: 
---

# tagMONCBSTRUCT structure


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

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms648730(v=VS.85).aspx">CONVCONTEXT</a></b>

The language information used to share data in different languages. 


### -field cbData

Type: <b>DWORD</b>

The amount, in bytes, of data being passed with the transaction. This value can be more than 32 bytes. 


### -field Data

Type: <b>DWORD[8]</b>

Contains the first 32 bytes of data being passed with the transaction (<code>8 * sizeof(DWORD)</code>). 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648730(v=VS.85).aspx">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648735(v=VS.85).aspx">MONERRSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648736(v=VS.85).aspx">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648737(v=VS.85).aspx">MONLINKSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648738(v=VS.85).aspx">MONMSGSTRUCT</a>



<b>Reference</b>
 

 

