---
UID: NF:ddeml.DdeUninitialize
title: DdeUninitialize function
author: windows-sdk-content
description: Frees all Dynamic Data Exchange Management Library (DDEML) resources associated with the calling application.
old-location: dataxchg\ddeuninitialize.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeuninitialize.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdeUninitialize, DdeUninitialize function [Data Exchange], _win32_DdeUninitialize, _win32_ddeuninitialize_cpp, dataxchg.ddeuninitialize, ddeml/DdeUninitialize, winui._win32_ddeuninitialize
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
 - DdeUninitialize
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeUninitialize function


## -description


Frees all Dynamic Data Exchange Management Library (DDEML) resources associated with the calling application. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a> function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -remarks



<b>DdeUninitialize</b> terminates any conversations currently open for the application. 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648749(v=VS.85).aspx">DdeDisconnect</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648750(v=VS.85).aspx">DdeDisconnectList</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

