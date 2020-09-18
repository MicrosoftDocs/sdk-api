---
UID: NS:ddeml.tagMONCONVSTRUCT
title: MONCONVSTRUCT (ddeml.h)
description: Contains information about a Dynamic Data Exchange (DDE) conversation. A DDE monitoring application can use this structure to obtain information about a conversation that has been established or has terminated.
helpviewer_keywords: ["*PMONCONVSTRUCT","MONCONVSTRUCT","MONCONVSTRUCT structure [Data Exchange]","PMONCONVSTRUCT","PMONCONVSTRUCT structure pointer [Data Exchange]","_win32_MONCONVSTRUCT_str","_win32_monconvstruct_str_cpp","dataxchg.monconvstruct_str","ddeml/MONCONVSTRUCT","ddeml/PMONCONVSTRUCT","winui._win32_monconvstruct_str"]
old-location: dataxchg\monconvstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monconvstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PMONCONVSTRUCT, MONCONVSTRUCT, MONCONVSTRUCT structure [Data Exchange], PMONCONVSTRUCT, PMONCONVSTRUCT structure pointer [Data Exchange], _win32_MONCONVSTRUCT_str, _win32_monconvstruct_str_cpp, dataxchg.monconvstruct_str, ddeml/MONCONVSTRUCT, ddeml/PMONCONVSTRUCT, winui._win32_monconvstruct_str'
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
req.typenames: MONCONVSTRUCT, *PMONCONVSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMONCONVSTRUCT
 - ddeml/tagMONCONVSTRUCT
 - PMONCONVSTRUCT
 - ddeml/PMONCONVSTRUCT
 - MONCONVSTRUCT
 - ddeml/MONCONVSTRUCT
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
 - MONCONVSTRUCT
---

# MONCONVSTRUCT structure


## -description

Contains information about a Dynamic Data Exchange (DDE) conversation. A DDE monitoring application can use this structure to obtain information about a conversation that has been established or has terminated.

## -struct-fields

### -field cb

Type: <b>UINT</b>

The structure's size, in bytes.

### -field fConnect

Type: <b>BOOL</b>

Indicates whether the conversation is currently established. A value of <b>TRUE</b> indicates the conversation is established; <b>FALSE</b> indicates it is not.

### -field dwTime

Type: <b>DWORD</b>

The Windows time at which the conversation was established or terminated. Windows time is the number of milliseconds that have elapsed since the system was booted.

### -field hTask

Type: <b>HANDLE</b>

A handle to a task (application instance) that is a partner in the conversation.

### -field hszSvc

Type: <b>HSZ</b>

A handle to the service name on which the conversation is established.

### -field hszTopic

Type: <b>HSZ</b>

A handle to the topic name on which the conversation is established.

### -field hConvClient

Type: <b>HCONV</b>

A handle to the client conversation.

### -field hConvServer

Type: <b>HCONV</b>

A handle to the server conversation.

## -remarks

Because string handles are local to the process, the <b>hszSvc</b> and <b>hszTopic</b> members are global atoms. Similarly, conversation handles are local to the instance; therefore, the <b>hConvClient</b> and <b>hConvServer</b> members are window handles. 

The <b>hConvClient</b> and <b>hConvServer</b> members of the <b>MONCONVSTRUCT</b> structure do not hold the same value as would be seen by the applications engaged in the conversation. Instead, they hold a globally unique pair of values that identify the conversation.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-moncbstruct">MONCBSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monerrstruct">MONERRSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monhszstructa">MONHSZSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monlinkstruct">MONLINKSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monmsgstruct">MONMSGSTRUCT</a>



<b>Reference</b>