---
UID: NF:ddeml.DdeDisconnect
title: DdeDisconnect function
author: windows-sdk-content
description: Terminates a conversation started by either the DdeConnect or DdeConnectList function and invalidates the specified conversation handle.
old-location: dataxchg\ddedisconnect.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddedisconnect.htm
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DdeDisconnect, DdeDisconnect function [Data Exchange], _win32_DdeDisconnect, _win32_ddedisconnect_cpp, dataxchg.ddedisconnect, ddeml/DdeDisconnect, winui._win32_ddedisconnect
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
 - DdeDisconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeDisconnect function


## -description


Terminates a conversation started by either the <a href="https://msdn.microsoft.com/6dfe446f-43e2-4dbc-940b-df9036c5f7aa">DdeConnect</a> or <a href="https://msdn.microsoft.com/26e49ba5-ff60-49cd-84af-f86055d69da0">DdeConnectList</a> function and invalidates the specified conversation handle. 


## -parameters




### -param hConv [in]

Type: <b>HCONV</b>

A handle to the active conversation to be terminated. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



Any incomplete transactions started before calling <b>DdeDisconnect</b> are immediately abandoned. The <a href="https://msdn.microsoft.com/22a9ec63-8a74-4829-ad02-d07dd0e8fa9b">XTYP_DISCONNECT</a> transaction is sent to the Dynamic Data Exchange (DDE) callback function of the partner in the conversation. Generally, only client applications must terminate conversations. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6dfe446f-43e2-4dbc-940b-df9036c5f7aa">DdeConnect</a>



<a href="https://msdn.microsoft.com/26e49ba5-ff60-49cd-84af-f86055d69da0">DdeConnectList</a>



<a href="https://msdn.microsoft.com/fd0527ef-116a-445a-b035-2abc161a6719">DdeDisconnectList</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/22a9ec63-8a74-4829-ad02-d07dd0e8fa9b">XTYP_DISCONNECT</a>
 

 

