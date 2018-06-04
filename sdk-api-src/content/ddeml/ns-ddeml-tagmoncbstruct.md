---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

Type: <b><a href="https://msdn.microsoft.com/0082c16a-5411-4ed2-a278-cc0f5b136133">CONVCONTEXT</a></b>

The language information used to share data in different languages. 


### -field cbData

Type: <b>DWORD</b>

The amount, in bytes, of data being passed with the transaction. This value can be more than 32 bytes. 


### -field Data

Type: <b>DWORD[8]</b>

Contains the first 32 bytes of data being passed with the transaction (<code>8 * sizeof(DWORD)</code>). 


## -see-also




<a href="https://msdn.microsoft.com/0082c16a-5411-4ed2-a278-cc0f5b136133">CONVCONTEXT</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/4e7647a0-c41e-4ec9-b441-01538e83aca3">MONERRSTRUCT</a>



<a href="https://msdn.microsoft.com/d5c6b5f8-e999-4f79-bf7c-b7d74a3e9b46">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/db02a191-677b-4fae-88ec-c2b500249837">MONLINKSTRUCT</a>



<a href="https://msdn.microsoft.com/7d971b35-0c88-42c3-83b9-93d5de6c95f9">MONMSGSTRUCT</a>



<b>Reference</b>
 

 

