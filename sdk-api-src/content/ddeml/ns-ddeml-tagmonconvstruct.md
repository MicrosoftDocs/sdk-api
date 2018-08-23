---
UID: NS:ddeml.tagMONCONVSTRUCT
title: tagMONCONVSTRUCT
author: windows-sdk-content
description: Contains information about a Dynamic Data Exchange (DDE) conversation. A DDE monitoring application can use this structure to obtain information about a conversation that has been established or has terminated.
old-location: dataxchg\monconvstruct_str.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementstructures\monconvstruct.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PMONCONVSTRUCT, MONCONVSTRUCT, MONCONVSTRUCT structure [Data Exchange], PMONCONVSTRUCT, PMONCONVSTRUCT structure pointer [Data Exchange], _win32_MONCONVSTRUCT_str, _win32_monconvstruct_str_cpp, dataxchg.monconvstruct_str, ddeml/MONCONVSTRUCT, ddeml/PMONCONVSTRUCT, tagMONCONVSTRUCT, winui._win32_monconvstruct_str"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddeml.h
req.include-header: Windows.h
req.redist: 
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
req.typenames: MONCONVSTRUCT, *PMONCONVSTRUCT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Ddeml.h
api_name:
 - MONCONVSTRUCT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# tagMONCONVSTRUCT structure


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



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/65bea5e0-ab86-4e00-9dbf-9809aab18616">MONCBSTRUCT</a>



<a href="https://msdn.microsoft.com/4e7647a0-c41e-4ec9-b441-01538e83aca3">MONERRSTRUCT</a>



<a href="https://msdn.microsoft.com/d5c6b5f8-e999-4f79-bf7c-b7d74a3e9b46">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/db02a191-677b-4fae-88ec-c2b500249837">MONLINKSTRUCT</a>



<a href="https://msdn.microsoft.com/7d971b35-0c88-42c3-83b9-93d5de6c95f9">MONMSGSTRUCT</a>



<b>Reference</b>
 

 

