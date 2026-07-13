---
UID: NF:ddeml.DdeQueryStringW
title: DdeQueryStringW function (ddeml.h)
description: Copies text associated with a string handle into a buffer. (Unicode)
helpviewer_keywords: ["DdeQueryString", "DdeQueryString function [Data Exchange]", "DdeQueryStringW", "_win32_DdeQueryString", "_win32_ddequerystring_cpp", "dataxchg.ddequerystring", "ddeml/DdeQueryString", "ddeml/DdeQueryStringW", "winui._win32_ddequerystring"]
old-location: dataxchg\ddequerystring.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddequerystring.htm
ms.date: 12/05/2018
ms.keywords: DdeQueryString, DdeQueryString function [Data Exchange], DdeQueryStringA, DdeQueryStringW, _win32_DdeQueryString, _win32_ddequerystring_cpp, dataxchg.ddequerystring, ddeml/DdeQueryString, ddeml/DdeQueryStringA, ddeml/DdeQueryStringW, winui._win32_ddequerystring
req.header: ddeml.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: DdeQueryStringW (Unicode) and DdeQueryStringA (ANSI)
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
 - DdeQueryStringW
 - ddeml/DdeQueryStringW
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
 - DdeQueryString
 - DdeQueryStringA
 - DdeQueryStringW
---

# DdeQueryStringW function


## -description

Copies text associated with a string handle into a buffer.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param hsz [in]

Type: <b>HSZ</b>

A handle to the string to copy. This handle must have been created by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a> function.

### -param psz [out, optional]

Type: <b>LPTSTR</b>

A pointer to a buffer that receives the string. To obtain the length of the string, this parameter should be set to <b>NULL</b>.

### -param cchMax [in]

Type: <b>DWORD</b>

The length, in 
					characters, of the buffer pointed to by the 
					<i>psz</i> parameter. For the ANSI version of the function, this is the number of bytes; for the Unicode version, this is the number of characters. If the string is longer than (
					<i>cchMax</i>– 1), it will be truncated. If the 
					<i>psz</i> parameter is set to <b>NULL</b>, this parameter is ignored.

### -param iCodePage [in]

Type: <b>int</b>

The code page used to render the string. This value should be either <b>CP_WINANSI</b> or <b>CP_WINUNICODE</b>.

## -returns

Type: <b>DWORD</b>

If the 
						<i>psz</i> parameter specified a valid pointer, the return value is the length, in 
						characters, of the returned text (not including the terminating null character). If the 
						<i>psz</i> parameter specified a <b>NULL</b> pointer, the return value is the length of the text associated with the 
						<i>hsz</i> parameter (not including the terminating null character). If an error occurs, the return value is 0L.

## -remarks

The string returned in the buffer is always null-terminated. If the string is longer than (
				<i>cchMax</i>– 1), only the first (
				<i>cchMax</i>– 1) characters of the string are copied. 

If the 
				<i>psz</i> parameter is <b>NULL</b>, the <b>DdeQueryString</b> function obtains the length, in bytes, of the string associated with the string handle. The length does not include the terminating null character. 





> [!NOTE]
> The ddeml.h header defines DdeQueryString as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecmpstringhandles">DdeCmpStringHandles</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddefreestringhandle">DdeFreeStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
