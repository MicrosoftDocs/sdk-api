---
UID: NF:ddeml.DdeDisconnectList
title: DdeDisconnectList function
author: windows-sdk-content
description: Destroys the specified conversation list and terminates all conversations associated with the list.
old-location: dataxchg\ddedisconnectlist.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddedisconnectlist.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdeDisconnectList, DdeDisconnectList function [Data Exchange], _win32_DdeDisconnectList, _win32_ddedisconnectlist_cpp, dataxchg.ddedisconnectlist, ddeml/DdeDisconnectList, winui._win32_ddedisconnectlist
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
req.typenames: DDEPOKE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeDisconnectList
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeDisconnectList function


## -description


Destroys the specified conversation list and terminates all conversations associated with the list. 


## -parameters




### -param hConvList [in]

Type: <b>HCONVLIST</b>

A handle to the conversation list. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/26e49ba5-ff60-49cd-84af-f86055d69da0">DdeConnectList</a> function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



An application can use the <a href="https://msdn.microsoft.com/e8564954-5abc-4ee1-b246-61fc023c5986">DdeDisconnect</a> function to terminate individual conversations in the list. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/6dfe446f-43e2-4dbc-940b-df9036c5f7aa">DdeConnect</a>



<a href="https://msdn.microsoft.com/26e49ba5-ff60-49cd-84af-f86055d69da0">DdeConnectList</a>



<a href="https://msdn.microsoft.com/e8564954-5abc-4ee1-b246-61fc023c5986">DdeDisconnect</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

