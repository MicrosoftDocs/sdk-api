---
UID: NF:ddeml.DdeDisconnect
title: DdeDisconnect function
author: windows-sdk-content
description: Terminates a conversation started by either the DdeConnect or DdeConnectList function and invalidates the specified conversation handle.
old-location: dataxchg\ddedisconnect.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddedisconnect.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DdeDisconnect, DdeDisconnect function [Data Exchange], _win32_DdeDisconnect, _win32_ddedisconnect_cpp, dataxchg.ddedisconnect, ddeml/DdeDisconnect, winui._win32_ddedisconnect
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DDEPOKE
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeDisconnect function


## -description


Terminates a conversation started by either the <a href="https://msdn.microsoft.com/library/ms648745(v=VS.85).aspx">DdeConnect</a> or <a href="https://msdn.microsoft.com/library/ms648746(v=VS.85).aspx">DdeConnectList</a> function and invalidates the specified conversation handle. 


## -parameters




### -param hConv [in]

Type: <b>HCONV</b>

A handle to the active conversation to be terminated. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/library/ms648755(v=VS.85).aspx">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



Any incomplete transactions started before calling <b>DdeDisconnect</b> are immediately abandoned. The <a href="https://msdn.microsoft.com/library/ms648720(v=VS.85).aspx">XTYP_DISCONNECT</a> transaction is sent to the Dynamic Data Exchange (DDE) callback function of the partner in the conversation. Generally, only client applications must terminate conversations. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms648745(v=VS.85).aspx">DdeConnect</a>



<a href="https://msdn.microsoft.com/library/ms648746(v=VS.85).aspx">DdeConnectList</a>



<a href="https://msdn.microsoft.com/library/ms648750(v=VS.85).aspx">DdeDisconnectList</a>



<a href="https://msdn.microsoft.com/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/library/ms648720(v=VS.85).aspx">XTYP_DISCONNECT</a>
 

 

