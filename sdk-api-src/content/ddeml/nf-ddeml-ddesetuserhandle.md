---
UID: NF:ddeml.DdeSetUserHandle
title: DdeSetUserHandle function
author: windows-sdk-content
description: Associates an application-defined value with a conversation handle or a transaction identifier. This is useful for simplifying the processing of asynchronous transactions. An application can use the DdeQueryConvInfo function to retrieve this value.
old-location: dataxchg\ddesetuserhandle.htm
old-project: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddesetuserhandle.htm
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: DdeSetUserHandle, DdeSetUserHandle function [Data Exchange], _win32_DdeSetUserHandle, _win32_ddesetuserhandle_cpp, dataxchg.ddesetuserhandle, ddeml/DdeSetUserHandle, winui._win32_ddesetuserhandle
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
 - DdeSetUserHandle
product: Windows
targetos: Windows
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
---

# DdeSetUserHandle function


## -description


Associates an application-defined value with a conversation handle or a transaction identifier. This is useful for simplifying the processing of asynchronous transactions. An application can use the <a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a> function to retrieve this value. 


## -parameters




### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation. 


### -param id [in]

Type: <b>DWORD</b>

The transaction identifier to associate with the value specified by the 
					<i>hUser</i> parameter. An application should set this parameter to QID_SYNC to associate 
					<i>hUser</i> with the conversation identified by the 
					<i>hConv</i> parameter. 


### -param hUser [in]

Type: <b>DWORD_PTR</b>

The value to be associated with the conversation handle. 


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="https://msdn.microsoft.com/ea7d758e-bf88-49a9-a51f-9be26376a1ed">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values: 




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/bf8faeef-9a06-4460-9dcc-6e74b9b0e72e">DdeQueryConvInfo</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

