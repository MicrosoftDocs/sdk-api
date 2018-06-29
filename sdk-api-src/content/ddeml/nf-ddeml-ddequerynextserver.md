---
UID: NF:ddeml.DdeQueryNextServer
title: DdeQueryNextServer function
author: windows-sdk-content
description: Retrieves the next conversation handle in the specified conversation list.
old-location: dataxchg\ddequerynextserver.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddequerynextserver.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DdeQueryNextServer, DdeQueryNextServer function [Data Exchange], _win32_DdeQueryNextServer, _win32_ddequerynextserver_cpp, dataxchg.ddequerynextserver, ddeml/DdeQueryNextServer, winui._win32_ddequerynextserver
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
 - DdeQueryNextServer
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeQueryNextServer function


## -description


Retrieves the next conversation handle in the specified conversation list. 


## -parameters




### -param hConvList [in]

Type: <b>HCONVLIST</b>

A handle to the conversation list. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/library/ms648746(v=VS.85).aspx">DdeConnectList</a> function. 


### -param hConvPrev [in]

Type: <b>HCONV</b>

A handle to the conversation handle previously returned by this function. If this parameter is 0L, the function returns the first conversation handle in the list. 


## -returns



Type: <b>HCONV</b>

If the list contains any more conversation handles, the return value is the next conversation handle in the list; otherwise, it is 0L. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms648746(v=VS.85).aspx">DdeConnectList</a>



<a href="https://msdn.microsoft.com/library/ms648750(v=VS.85).aspx">DdeDisconnectList</a>



<a href="https://msdn.microsoft.com/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

