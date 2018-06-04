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

# tagMONMSGSTRUCT structure


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

Type: <b><a href="https://msdn.microsoft.com/d556c210-8a4a-4e43-a596-3350a89609fe">DDEML_MSG_HOOK_DATA</a></b>

Additional information about the DDE message. 


## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/d556c210-8a4a-4e43-a596-3350a89609fe">DDEML_MSG_HOOK_DATA</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<a href="https://msdn.microsoft.com/65bea5e0-ab86-4e00-9dbf-9809aab18616">MONCBSTRUCT</a>



<a href="https://msdn.microsoft.com/24fe9042-7b9f-4139-a9b5-d8c72529d897">MONCONVSTRUCT</a>



<a href="https://msdn.microsoft.com/4e7647a0-c41e-4ec9-b441-01538e83aca3">MONERRSTRUCT</a>



<a href="https://msdn.microsoft.com/d5c6b5f8-e999-4f79-bf7c-b7d74a3e9b46">MONHSZSTRUCT</a>



<a href="https://msdn.microsoft.com/db02a191-677b-4fae-88ec-c2b500249837">MONLINKSTRUCT</a>



<b>Reference</b>
 

 

