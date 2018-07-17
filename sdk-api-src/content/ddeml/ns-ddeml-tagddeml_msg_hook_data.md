---
UID: NS:ddeml.tagDDEML_MSG_HOOK_DATA
title: tagDDEML_MSG_HOOK_DATA
author: windows-sdk-content
description: Contains information about a Dynamic Data Exchange (DDE) message, and provides read access to the data referenced by the message. This structure is intended to be used by a Dynamic Data Exchange Management Library (DDEML) monitoring application.
old-location: dataxchg\ddeml_msg_hook_data_str.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\ddeml_msg_hook_data.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: "*PDDEML_MSG_HOOK_DATA, DDEML_MSG_HOOK_DATA, DDEML_MSG_HOOK_DATA structure [Data Exchange], PDDEML_MSG_HOOK_DATA, PDDEML_MSG_HOOK_DATA structure pointer [Data Exchange], _win32_DDEML_MSG_HOOK_DATA_str, _win32_ddeml_msg_hook_data_str_cpp, dataxchg.ddeml_msg_hook_data_str, ddeml/DDEML_MSG_HOOK_DATA, ddeml/PDDEML_MSG_HOOK_DATA, tagDDEML_MSG_HOOK_DATA, winui._win32_ddeml_msg_hook_data_str"
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
tech.root: 
req.typenames: DDEML_MSG_HOOK_DATA, *PDDEML_MSG_HOOK_DATA
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
req.lib: 
req.dll: 
req.irql: 
---

# tagDDEML_MSG_HOOK_DATA structure


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



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/65bea5e0-ab86-4e00-9dbf-9809aab18616">MONCBSTRUCT</a>



<a href="https://msdn.microsoft.com/24fe9042-7b9f-4139-a9b5-d8c72529d897">MONCONVSTRUCT</a>



<a href="https://msdn.microsoft.com/4e7647a0-c41e-4ec9-b441-01538e83aca3">MONERRSTRUCT</a>



<a href="https://msdn.microsoft.com/d5c6b5f8-e999-4f79-bf7c-b7d74a3e9b46">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/db02a191-677b-4fae-88ec-c2b500249837">MONLINKSTRUCT</a>



<a href="https://msdn.microsoft.com/7d971b35-0c88-42c3-83b9-93d5de6c95f9">MONMSGSTRUCT</a>



<b>Reference</b>
 

 

