---
UID: NF:ddeml.DdeCreateStringHandleW
title: DdeCreateStringHandleW function
author: windows-sdk-content
description: Creates a handle that identifies the specified string. A Dynamic Data Exchange (DDE) client or server application can pass the string handle as a parameter to other Dynamic Data Exchange Management Library (DDEML) functions.
old-location: dataxchg\ddecreatestringhandle.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddecreatestringhandle.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdeCreateStringHandle, DdeCreateStringHandle function [Data Exchange], DdeCreateStringHandleA, DdeCreateStringHandleW, _win32_DdeCreateStringHandle, _win32_ddecreatestringhandle_cpp, dataxchg.ddecreatestringhandle, ddeml/DdeCreateStringHandle, ddeml/DdeCreateStringHandleA, ddeml/DdeCreateStringHandleW, winui._win32_ddecreatestringhandle
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
req.unicode-ansi: DdeCreateStringHandleW (Unicode) and DdeCreateStringHandleA (ANSI)
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
 - DdeCreateStringHandle
 - DdeCreateStringHandleA
 - DdeCreateStringHandleW
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeCreateStringHandleW function


## -description


Creates a handle that identifies the specified string. A Dynamic Data Exchange (DDE) client or server application can pass the string handle as a parameter to other Dynamic Data Exchange Management Library (DDEML) functions. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a> function. 


### -param psz [in]

Type: <b>LPTSTR</b>

The null-terminated string for which a handle is to be created. This string can be up to 255 characters. The reason for this limit is that DDEML string management functions are implemented using atoms. 


### -param iCodePage [in]

Type: <b>int</b>

The code page to be used to render the string. This value should be either <b>CP_WINANSI</b> (the default code page) or CP_WINUNICODE, depending on whether the ANSI or Unicode version of <a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a> was called by the client application. 


## -returns



Type: <b>HSZ</b>

If the function succeeds, the return value is a string handle.

If the function fails, the return value is 0L. 

The <a href="https://msdn.microsoft.com/en-us/library/ms648755(v=VS.85).aspx">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -remarks



The value of a string handle is not related to the case of the string it identifies. 

When an application either creates a string handle or receives one in the callback function and then uses the <a href="https://msdn.microsoft.com/en-us/library/ms648758(v=VS.85).aspx">DdeKeepStringHandle</a> function to keep it, the application must free that string handle when it is no longer needed. 

An instance-specific string handle cannot be mapped from string handle to string and back to string handle. This is shown in the following example, in which the <a href="https://msdn.microsoft.com/en-us/library/ms648763(v=VS.85).aspx">DdeQueryString</a> function creates a string from a string handle and <b>DdeCreateStringHandle</b> creates a string handle from that string, but the two handles are not the same: 


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```





## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/ms648740(v=VS.85).aspx">DdeAccessData</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648744(v=VS.85).aspx">DdeCmpStringHandles</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648753(v=VS.85).aspx">DdeFreeStringHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648757(v=VS.85).aspx">DdeInitialize</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648758(v=VS.85).aspx">DdeKeepStringHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648763(v=VS.85).aspx">DdeQueryString</a>



<a href="https://msdn.microsoft.com/en-us/library/ms648712(v=VS.85).aspx">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

