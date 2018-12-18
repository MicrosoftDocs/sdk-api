---
UID: NS:ddeml.tagDDEML_MSG_HOOK_DATA
title: DDEML_MSG_HOOK_DATA
author: windows-sdk-content
description: Contains information about a Dynamic Data Exchange (DDE) message, and provides read access to the data referenced by the message. This structure is intended to be used by a Dynamic Data Exchange Management Library (DDEML) monitoring application.
old-location: dataxchg\ddeml_msg_hook_data_str.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\ddeml_msg_hook_data.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PDDEML_MSG_HOOK_DATA, DDEML_MSG_HOOK_DATA, DDEML_MSG_HOOK_DATA structure [Data Exchange], PDDEML_MSG_HOOK_DATA, PDDEML_MSG_HOOK_DATA structure pointer [Data Exchange], _win32_DDEML_MSG_HOOK_DATA_str, _win32_ddeml_msg_hook_data_str_cpp, dataxchg.ddeml_msg_hook_data_str, ddeml/DDEML_MSG_HOOK_DATA, ddeml/PDDEML_MSG_HOOK_DATA, winui._win32_ddeml_msg_hook_data_str"
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
 - DDEML_MSG_HOOK_DATA
product: Windows
targetos: Windows
req.typenames: DDEML_MSG_HOOK_DATA, *PDDEML_MSG_HOOK_DATA
req.redist: 
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



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648733(v=VS.85).aspx">MONCBSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648734(v=VS.85).aspx">MONCONVSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648735(v=VS.85).aspx">MONERRSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648736(v=VS.85).aspx">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648737(v=VS.85).aspx">MONLINKSTRUCT</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648738(v=VS.85).aspx">MONMSGSTRUCT</a>



<b>Reference</b>
 

 

