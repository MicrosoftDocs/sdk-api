---
UID: NF:ddeml.DdeFreeStringHandle
title: DdeFreeStringHandle function
author: windows-sdk-content
description: Frees a string handle in the calling application.
old-location: dataxchg\ddefreestringhandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddefreestringhandle.htm
ms.author: windowssdkdev
ms.date: 11/16/2018
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

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 


### -param hsz [in]

Type: <b>HSZ</b>

A handle to the string handle to be freed. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a> function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -remarks



An application can free string handles it creates with <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a> but should not free those that the system passed to the application's Dynamic Data Exchange (DDE) callback function or those returned in the <a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a> structure by the <a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a> function. 




## -see-also




<a href="https://msdn.microsoft.com/fb90f16f-d17c-4123-b821-602e8a5d25b1">CONVINFO</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/87586deb-7862-4a52-8787-cb14edc4e053">DdeCmpStringHandles</a>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/ecef0207-061c-451a-a911-1b821bbe099d">DdeKeepStringHandle</a>



<a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a>



<a href="https://msdn.microsoft.com/d2130568-b72f-467d-b4c5-a09a3e55110d">DdeQueryString</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

