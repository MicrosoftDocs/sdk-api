---
UID: NF:ddeml.DdeFreeStringHandle
title: DdeFreeStringHandle function
author: windows-sdk-content
description: Frees a string handle in the calling application.
old-location: dataxchg\ddefreestringhandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddefreestringhandle.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DdeFreeStringHandle, DdeFreeStringHandle function [Data Exchange], _win32_DdeFreeStringHandle, _win32_ddefreestringhandle_cpp, dataxchg.ddefreestringhandle, ddeml/DdeFreeStringHandle, winui._win32_ddefreestringhandle
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
 - DdeFreeStringHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeFreeStringHandle function


## -description


Frees a string handle in the calling application. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a> function. 


### -param hsz [in]

Type: <b>HSZ</b>

A handle to the string handle to be freed. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a> function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -remarks



An application can free string handles it creates with <a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a> but should not free those that the system passed to the application's Dynamic Data Exchange (DDE) callback function or those returned in the <a href="https://msdn.microsoft.com/en-us/library/ms648731(v=VS.85).aspx">CONVINFO</a> structure by the <a href="https://msdn.microsoft.com/en-us/library/ms648761(v=VS.85).aspx">DdeQueryConvInfo</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms648731(v=VS.85).aspx">CONVINFO</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648744(v=VS.85).aspx">DdeCmpStringHandles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648748(v=VS.85).aspx">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648758(v=VS.85).aspx">DdeKeepStringHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648761(v=VS.85).aspx">DdeQueryConvInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648763(v=VS.85).aspx">DdeQueryString</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

