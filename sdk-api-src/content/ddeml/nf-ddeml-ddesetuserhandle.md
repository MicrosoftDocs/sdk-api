---
UID: NF:ddeml.DdeSetUserHandle
title: DdeSetUserHandle function (ddeml.h)
description: Associates an application-defined value with a conversation handle or a transaction identifier. This is useful for simplifying the processing of asynchronous transactions. An application can use the DdeQueryConvInfo function to retrieve this value.
helpviewer_keywords: ["DdeSetUserHandle","DdeSetUserHandle function [Data Exchange]","_win32_DdeSetUserHandle","_win32_ddesetuserhandle_cpp","dataxchg.ddesetuserhandle","ddeml/DdeSetUserHandle","winui._win32_ddesetuserhandle"]
old-location: dataxchg\ddesetuserhandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddesetuserhandle.htm
ms.date: 12/05/2018
ms.keywords: DdeSetUserHandle, DdeSetUserHandle function [Data Exchange], _win32_DdeSetUserHandle, _win32_ddesetuserhandle_cpp, dataxchg.ddesetuserhandle, ddeml/DdeSetUserHandle, winui._win32_ddesetuserhandle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdeSetUserHandle
 - ddeml/DdeSetUserHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - User32.dll
api_name:
 - DdeSetUserHandle
---

# DdeSetUserHandle function


## -description

Associates an application-defined value with a conversation handle or a transaction identifier. This is useful for simplifying the processing of asynchronous transactions. An application can use the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a> function to retrieve this value.

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

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddequeryconvinfo">DdeQueryConvInfo</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>