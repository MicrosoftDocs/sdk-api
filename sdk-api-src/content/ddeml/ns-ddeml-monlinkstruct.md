---
UID: NS:ddeml.tagMONLINKSTRUCT
title: MONLINKSTRUCT (ddeml.h)
description: Contains information about a Dynamic Data Exchange (DDE) advise loop. A DDE monitoring application can use this structure to obtain information about an advise loop that has started or ended.
helpviewer_keywords: ["*PMONLINKSTRUCT","MONLINKSTRUCT","MONLINKSTRUCT structure [Data Exchange]","PMONLINKSTRUCT","PMONLINKSTRUCT structure pointer [Data Exchange]","_win32_MONLINKSTRUCT_str","_win32_monlinkstruct_str_cpp","dataxchg.monlinkstruct_str","ddeml/MONLINKSTRUCT","ddeml/PMONLINKSTRUCT","winui._win32_monlinkstruct_str"]
old-location: dataxchg\monlinkstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monlinkstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PMONLINKSTRUCT, MONLINKSTRUCT, MONLINKSTRUCT structure [Data Exchange], PMONLINKSTRUCT, PMONLINKSTRUCT structure pointer [Data Exchange], _win32_MONLINKSTRUCT_str, _win32_monlinkstruct_str_cpp, dataxchg.monlinkstruct_str, ddeml/MONLINKSTRUCT, ddeml/PMONLINKSTRUCT, winui._win32_monlinkstruct_str'
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
req.typenames: MONLINKSTRUCT, *PMONLINKSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMONLINKSTRUCT
 - ddeml/tagMONLINKSTRUCT
 - PMONLINKSTRUCT
 - ddeml/PMONLINKSTRUCT
 - MONLINKSTRUCT
 - ddeml/MONLINKSTRUCT
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
 - MONLINKSTRUCT
---

# MONLINKSTRUCT structure


## -description

Contains information about a Dynamic Data Exchange (DDE) advise loop. A DDE monitoring application can use this structure to obtain information about an advise loop that has started or ended.

## -struct-fields

### -field cb

Type: <b>UINT</b>

The structure's size, in bytes.

### -field dwTime

Type: <b>DWORD</b>

The Windows time at which the advise loop was started or ended. Windows time is the number of milliseconds that have elapsed since the system was booted.

### -field hTask

Type: <b>HANDLE</b>

A handle to a task (application instance) that is a partner in the advise loop.

### -field fEstablished

Type: <b>BOOL</b>

Indicates whether an advise loop was successfully established. A value of <b>TRUE</b> indicates an advise loop was established; <b>FALSE</b> indicates it was not.

### -field fNoData

Type: <b>BOOL</b>

Indicates whether the XTYPF_NODATA flag is set for the advise loop. A value of <b>TRUE</b> indicates the flag is set; <b>FALSE</b> indicates it is not.

### -field hszSvc

Type: <b>HSZ</b>

A handle to the service name of the server in the advise loop.

### -field hszTopic

Type: <b>HSZ</b>

A handle to the topic name on which the advise loop is established.

### -field hszItem

Type: <b>HSZ</b>

A handle to the item name that is the subject of the advise loop.

### -field wFmt

Type: <b>UINT</b>

The format of the data exchanged (if any) during the advise loop.

### -field fServer

Type: <b>BOOL</b>

Indicates whether the link notification came from the server. A value of <b>TRUE</b> indicates the notification came from the server; <b>FALSE</b> indicates otherwise.

### -field hConvServer

Type: <b>HCONV</b>

A handle to the server conversation.

### -field hConvClient

Type: <b>HCONV</b>

A handle to the client conversation.

## -remarks

Because string handles are local to the process, the <b>hszSvc</b>, <b>hszTopic</b>, and <b>hszItem</b> members are global atoms. 

The 
				<b>hConvClient</b> and <b>hConvServer</b> members of the <b>MONLINKSTRUCT</b> structure do not hold the same value as would be seen by the applications engaged in the conversation. Instead, they hold a globally unique pair of values that identify the conversation.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-moncbstruct">MONCBSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monerrstruct">MONERRSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monhszstructa">MONHSZSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monmsgstruct">MONMSGSTRUCT</a>



<b>Reference</b>