---
UID: NF:ddeml.DdeKeepStringHandle
title: DdeKeepStringHandle function
author: windows-sdk-content
description: Increments the usage count associated with the specified handle.
old-location: dataxchg\ddekeepstringhandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddekeepstringhandle.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DdeKeepStringHandle, DdeKeepStringHandle function [Data Exchange], _win32_DdeKeepStringHandle, _win32_ddekeepstringhandle_cpp, dataxchg.ddekeepstringhandle, ddeml/DdeKeepStringHandle, winui._win32_ddekeepstringhandle
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
 - DdeKeepStringHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeKeepStringHandle function


## -description


Increments the usage count associated with the specified handle. This function enables an application to save a string handle passed to the application's Dynamic Data Exchange (DDE) callback function. Otherwise, a string handle passed to the callback function is deleted when the callback function returns. This function should also be used to keep a copy of a string handle referenced by the <a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a> structure returned by the <a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a> function. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 


### -param hsz [in]

Type: <b>HSZ</b>

A handle to the string handle to be saved. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -see-also




<a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/93228467-345b-4ff1-942e-2d75a53bce65">DdeFreeStringHandle</a>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a>



<a href="https://msdn.microsoft.com/d2130568-b72f-467d-b4c5-a09a3e55110d">DdeQueryString</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

