---
UID: NS:ddeml.tagDDEML_MSG_HOOK_DATA
title: DDEML_MSG_HOOK_DATA (ddeml.h)
description: Contains information about a Dynamic Data Exchange (DDE) message, and provides read access to the data referenced by the message. This structure is intended to be used by a Dynamic Data Exchange Management Library (DDEML) monitoring application.
helpviewer_keywords: ["*PDDEML_MSG_HOOK_DATA","DDEML_MSG_HOOK_DATA","DDEML_MSG_HOOK_DATA structure [Data Exchange]","PDDEML_MSG_HOOK_DATA","PDDEML_MSG_HOOK_DATA structure pointer [Data Exchange]","_win32_DDEML_MSG_HOOK_DATA_str","_win32_ddeml_msg_hook_data_str_cpp","dataxchg.ddeml_msg_hook_data_str","ddeml/DDEML_MSG_HOOK_DATA","ddeml/PDDEML_MSG_HOOK_DATA","winui._win32_ddeml_msg_hook_data_str"]
old-location: dataxchg\ddeml_msg_hook_data_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\ddeml_msg_hook_data.htm
ms.date: 12/05/2018
ms.keywords: '*PDDEML_MSG_HOOK_DATA, DDEML_MSG_HOOK_DATA, DDEML_MSG_HOOK_DATA structure [Data Exchange], PDDEML_MSG_HOOK_DATA, PDDEML_MSG_HOOK_DATA structure pointer [Data Exchange], _win32_DDEML_MSG_HOOK_DATA_str, _win32_ddeml_msg_hook_data_str_cpp, dataxchg.ddeml_msg_hook_data_str, ddeml/DDEML_MSG_HOOK_DATA, ddeml/PDDEML_MSG_HOOK_DATA, winui._win32_ddeml_msg_hook_data_str'
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
req.typenames: DDEML_MSG_HOOK_DATA, *PDDEML_MSG_HOOK_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagDDEML_MSG_HOOK_DATA
 - ddeml/tagDDEML_MSG_HOOK_DATA
 - PDDEML_MSG_HOOK_DATA
 - ddeml/PDDEML_MSG_HOOK_DATA
 - DDEML_MSG_HOOK_DATA
 - ddeml/DDEML_MSG_HOOK_DATA
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
 - DDEML_MSG_HOOK_DATA
---

# DDEML_MSG_HOOK_DATA structure


## -description

Contains information about a Dynamic Data Exchange (DDE) message, and provides read access to the data referenced by the message. This structure is intended to be used by a Dynamic Data Exchange Management Library (DDEML) monitoring application.

## -struct-fields

### -field uiLo

Type: <b>UINT_PTR</b>

The unpacked low-order word of the <i>lParam</i> parameter associated with the DDE message.

### -field uiHi

Type: <b>UINT_PTR</b>

The unpacked high-order word of the <i>lParam</i> parameter associated with the DDE message.

### -field cbData

Type: <b>DWORD</b>

The amount of data being passed with the message, in bytes. This value can be greater than 32.

### -field Data

Type: <b>DWORD[8]</b>

The first 32 bytes of data being passed with the message (<code>8 * sizeof(DWORD)</code>).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-moncbstruct">MONCBSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monconvstruct">MONCONVSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monerrstruct">MONERRSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monhszstructa">MONHSZSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monlinkstruct">MONLINKSTRUCT</a>



<a href="/windows/desktop/api/ddeml/ns-ddeml-monmsgstruct">MONMSGSTRUCT</a>



<b>Reference</b>