---
UID: NF:ddeml.DdeFreeStringHandle
title: DdeFreeStringHandle function (ddeml.h)
author: windows-sdk-content
description: Frees a string handle in the calling application.
old-location: dataxchg\ddefreestringhandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddefreestringhandle.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DdeFreeStringHandle, DdeFreeStringHandle function [Data Exchange], _win32_DdeFreeStringHandle, _win32_ddefreestringhandle_cpp, dataxchg.ddefreestringhandle, ddeml/DdeFreeStringHandle, winui._win32_ddefreestringhandle
ms.topic: function
f1_keywords: ["ddeml/DdeFreeStringHandle"]
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
ms.custom: 19H1
---

# DdeFreeStringHandle function


## -description


Frees a string handle in the calling application. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function. 


### -param hsz [in]

Type: <b>HSZ</b>

A handle to the string handle to be freed. This handle must have been created by a previous call to the <a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a> function. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 




## -remarks



An application can free string handles it creates with <a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a> but should not free those that the system passed to the application's Dynamic Data Exchange (DDE) callback function or those returned in the <a href="https://docs.microsoft.com/windows/desktop/api/ddeml/ns-ddeml-tagconvinfo">CONVINFO</a> structure by the <a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a> function. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddeml/ns-ddeml-tagconvinfo">CONVINFO</a>



<b>Conceptual</b>



<a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddecmpstringhandles">DdeCmpStringHandles</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddekeepstringhandle">DdeKeepStringHandle</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddeml/nf-ddeml-ddequerystringa">DdeQueryString</a>



<a href="https://docs.microsoft.com/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

