---
UID: NF:ddeml.DdeCreateStringHandleA
title: DdeCreateStringHandleA function (ddeml.h)
description: Creates a handle that identifies the specified string. A Dynamic Data Exchange (DDE) client or server application can pass the string handle as a parameter to other Dynamic Data Exchange Management Library (DDEML) functions. (ANSI)
helpviewer_keywords: ["DdeCreateStringHandleA", "ddeml/DdeCreateStringHandleA"]
old-location: dataxchg\ddecreatestringhandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddecreatestringhandle.htm
ms.date: 12/05/2018
ms.keywords: DdeCreateStringHandle, DdeCreateStringHandle function [Data Exchange], DdeCreateStringHandleA, DdeCreateStringHandleW, _win32_DdeCreateStringHandle, _win32_ddecreatestringhandle_cpp, dataxchg.ddecreatestringhandle, ddeml/DdeCreateStringHandle, ddeml/DdeCreateStringHandleA, ddeml/DdeCreateStringHandleW, winui._win32_ddecreatestringhandle
req.header: ddeml.h
req.include-header: Windows.h
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
req.lib: User32.lib
req.dll: User32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdeCreateStringHandleA
 - ddeml/DdeCreateStringHandleA
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
 - DdeCreateStringHandle
 - DdeCreateStringHandleA
 - DdeCreateStringHandleW
---

# DdeCreateStringHandleA function


## -description

Creates a handle that identifies the specified string. A Dynamic Data Exchange (DDE) client or server application can pass the string handle as a parameter to other Dynamic Data Exchange Management Library (DDEML) functions.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param psz [in]

Type: <b>LPTSTR</b>

The null-terminated string for which a handle is to be created. This string can be up to 255 characters. The reason for this limit is that DDEML string management functions are implemented using atoms.

### -param iCodePage [in]

Type: <b>int</b>

The code page to be used to render the string. This value should be either <b>CP_WINANSI</b> (the default code page) or CP_WINUNICODE, depending on whether the ANSI or Unicode version of <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> was called by the client application.

## -returns

Type: <b>HSZ</b>

If the function succeeds, the return value is a string handle.

If the function fails, the return value is 0L. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

The value of a string handle is not related to the case of the string it identifies. 

When an application either creates a string handle or receives one in the callback function and then uses the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddekeepstringhandle">DdeKeepStringHandle</a> function to keep it, the application must free that string handle when it is no longer needed. 

An instance-specific string handle cannot be mapped from string handle to string and back to string handle. This is shown in the following example, in which the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddequerystringa">DdeQueryString</a> function creates a string from a string handle and <b>DdeCreateStringHandle</b> creates a string handle from that string, but the two handles are not the same: 


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```






> [!NOTE]
> The ddeml.h header defines DdeCreateStringHandle as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeaccessdata">DdeAccessData</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecmpstringhandles">DdeCmpStringHandles</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddefreestringhandle">DdeFreeStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddekeepstringhandle">DdeKeepStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddequerystringa">DdeQueryString</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
