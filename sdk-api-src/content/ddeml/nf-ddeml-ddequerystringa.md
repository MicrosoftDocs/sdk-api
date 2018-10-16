---
UID: NF:ddeml.DdeQueryStringA
title: DdeQueryStringA function
author: windows-sdk-content
description: Copies text associated with a string handle into a buffer.
old-location: dataxchg\ddequerystring.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddequerystring.htm
ms.author: windowssdkdev
ms.date: 10/12/2018
ms.keywords: DdeQueryString, DdeQueryString function [Data Exchange], DdeQueryStringA, DdeQueryStringW, _win32_DdeQueryString, _win32_ddequerystring_cpp, dataxchg.ddequerystring, ddeml/DdeQueryString, ddeml/DdeQueryStringA, ddeml/DdeQueryStringW, winui._win32_ddequerystring
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
req.unicode-ansi: DdeQueryStringW (Unicode) and DdeQueryStringA (ANSI)
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
 - DdeQueryString
 - DdeQueryStringA
 - DdeQueryStringW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DdeQueryStringA function


## -description


Copies text associated with a string handle into a buffer. 


## -parameters




### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a> function. 


### -param hsz [in]

Type: <b>HSZ</b>

A handle to the string to copy. This handle must have been created by a previous call to the <a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a> function. 


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




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/87586deb-7862-4a52-8787-cb14edc4e053">DdeCmpStringHandles</a>



<a href="https://msdn.microsoft.com/561bbf80-cc73-4fe1-ba95-837d515834eb">DdeCreateStringHandle</a>



<a href="https://msdn.microsoft.com/93228467-345b-4ff1-942e-2d75a53bce65">DdeFreeStringHandle</a>



<a href="https://msdn.microsoft.com/ea679d2b-8c03-4706-b6a8-37a99c6d61d1">DdeInitialize</a>



<a href="https://msdn.microsoft.com/f22d4a10-58b9-4f62-bbc3-3cbeb3246923">Dynamic Data Exchange Management Library</a>



<b>Reference</b>
 

 

