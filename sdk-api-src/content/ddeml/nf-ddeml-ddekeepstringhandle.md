---
UID: NF:ddeml.DdeKeepStringHandle
title: DdeKeepStringHandle function
author: windows-sdk-content
description: Increments the usage count associated with the specified handle.
old-location: dataxchg\ddekeepstringhandle.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddekeepstringhandle.htm
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DdeKeepStringHandle, DdeKeepStringHandle function [Data Exchange], _win32_DdeKeepStringHandle, _win32_ddekeepstringhandle_cpp, dataxchg.ddekeepstringhandle, ddeml/DdeKeepStringHandle, winui._win32_ddekeepstringhandle
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
 - DdeKeepStringHandle
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeKeepStringHandle function


## -description


Increments the usage count associated with the specified handle. This function enables an application to save a string handle passed to the application's Dynamic Data Exchange (DDE) callback function. Otherwise, a string handle passed to the callback function is deleted when the callback function returns. This function should also be used to keep a copy of a string handle referenced by the <a href="https://msdn.microsoft.com/library/ms648731(v=VS.85).aspx">CONVINFO</a> structure returned by the <a href="https://msdn.microsoft.com/library/ms648761(v=VS.85).aspx">DdeQueryConvInfo</a> function. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/library/ms648757(v=VS.85).aspx">DdeInitialize</a> function. 


### -param hsz [in]

Type: <b>HSZ</b>

A handle to the string handle to be saved. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -see-also




<a href="https://msdn.microsoft.com/library/ms648731(v=VS.85).aspx">CONVINFO</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/library/ms648753(v=VS.85).aspx">DdeFreeStringHandle</a>



<a href="https://msdn.microsoft.com/library/ms648757(v=VS.85).aspx">DdeInitialize</a>



<a href="https://msdn.microsoft.com/library/ms648761(v=VS.85).aspx">DdeQueryConvInfo</a>



<a href="https://msdn.microsoft.com/library/ms648763(v=VS.85).aspx">DdeQueryString</a>



<a href="https://msdn.microsoft.com/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

