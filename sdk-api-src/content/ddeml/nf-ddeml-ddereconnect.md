---
UID: NF:ddeml.DdeReconnect
title: DdeReconnect function
author: windows-sdk-content
description: Enables a client Dynamic Data Exchange Management Library (DDEML) application to attempt to reestablish a conversation with a service that has terminated a conversation with the client.
old-location: dataxchg\ddereconnect.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddereconnect.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DdeReconnect, DdeReconnect function [Data Exchange], _win32_DdeReconnect, _win32_ddereconnect_cpp, dataxchg.ddereconnect, ddeml/DdeReconnect, winui._win32_ddereconnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeReconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeReconnect function


## -description


Enables a client <a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a> (DDEML) application to attempt to reestablish a conversation with a service that has terminated a conversation with the client. When the conversation is reestablished, the Dynamic Data Exchange Management Library (DDEML) attempts to reestablish any preexisting advise loops. 


## -parameters




### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation to be reestablished. A client must have obtained the conversation handle by a previous call to the <a href="https://msdn.microsoft.com/6dfe446f-43e2-4dbc-940b-df9036c5f7aa">DdeConnect</a> function or from an <a href="https://msdn.microsoft.com/22a9ec63-8a74-4829-ad02-d07dd0e8fa9b">XTYP_DISCONNECT</a> transaction. 


## -returns



Type: <b>HCONV</b>

If the function succeeds, the return value is the handle to the reestablished conversation.

If the function fails, the return value is 0L. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6dfe446f-43e2-4dbc-940b-df9036c5f7aa">DdeConnect</a>



<a href="https://msdn.microsoft.com/e8564954-5abc-4ee1-b246-61fc023c5986">DdeDisconnect</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

