---
UID: NS:ddeml.tagMONMSGSTRUCT
title: MONMSGSTRUCT (ddeml.h)
description: Contains information about a Dynamic Data Exchange (DDE) message. A DDE monitoring application can use this structure to obtain information about a DDE message that was sent or posted.
helpviewer_keywords: ["*PMONMSGSTRUCT","MONMSGSTRUCT","MONMSGSTRUCT structure [Data Exchange]","PMONMSGSTRUCT","PMONMSGSTRUCT structure pointer [Data Exchange]","_win32_MONMSGSTRUCT_str","_win32_monmsgstruct_str_cpp","dataxchg.monmsgstruct_str","ddeml/MONMSGSTRUCT","ddeml/PMONMSGSTRUCT","winui._win32_monmsgstruct_str"]
old-location: dataxchg\monmsgstruct_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monmsgstruct.htm
ms.date: 12/05/2018
ms.keywords: '*PMONMSGSTRUCT, MONMSGSTRUCT, MONMSGSTRUCT structure [Data Exchange], PMONMSGSTRUCT, PMONMSGSTRUCT structure pointer [Data Exchange], _win32_MONMSGSTRUCT_str, _win32_monmsgstruct_str_cpp, dataxchg.monmsgstruct_str, ddeml/MONMSGSTRUCT, ddeml/PMONMSGSTRUCT, winui._win32_monmsgstruct_str'
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
req.typenames: MONMSGSTRUCT, *PMONMSGSTRUCT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagMONMSGSTRUCT
 - ddeml/tagMONMSGSTRUCT
 - PMONMSGSTRUCT
 - ddeml/PMONMSGSTRUCT
 - MONMSGSTRUCT
 - ddeml/MONMSGSTRUCT
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
 - MONMSGSTRUCT
---

# MONMSGSTRUCT structure


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

Type: <b><a href="/windows/desktop/api/ddeml/ns-ddeml-ddeml_msg_hook_data">DDEML_MSG_HOOK_DATA</a></b>

Additional information about the DDE message.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/ns-ddeml-ddeml_msg_hook_data">DDEML_MSG_HOOK_DATA</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-moncbstruct">MONCBSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monconvstruct">MONCONVSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monerrstruct">MONERRSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monhszstructa">MONHSZSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monlinkstruct">MONLINKSTRUCT</a>



<b>Reference</b>