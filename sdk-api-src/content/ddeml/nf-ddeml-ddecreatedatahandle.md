---
UID: NF:ddeml.DdeCreateDataHandle
title: DdeCreateDataHandle function (ddeml.h)
description: Creates a Dynamic Data Exchange (DDE) object and fills the object with data from the specified buffer. A DDE application uses this function during transactions that involve passing data to the partner application.
helpviewer_keywords: ["DdeCreateDataHandle","DdeCreateDataHandle function [Data Exchange]","_win32_DdeCreateDataHandle","_win32_ddecreatedatahandle_cpp","dataxchg.ddecreatedatahandle","ddeml/DdeCreateDataHandle","winui._win32_ddecreatedatahandle"]
old-location: dataxchg\ddecreatedatahandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddecreatedatahandle.htm
ms.date: 12/05/2018
ms.keywords: DdeCreateDataHandle, DdeCreateDataHandle function [Data Exchange], _win32_DdeCreateDataHandle, _win32_ddecreatedatahandle_cpp, dataxchg.ddecreatedatahandle, ddeml/DdeCreateDataHandle, winui._win32_ddecreatedatahandle
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
 - DdeCreateDataHandle
 - ddeml/DdeCreateDataHandle
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
 - DdeCreateDataHandle
---

# DdeCreateDataHandle function


## -description

Creates a Dynamic Data Exchange (DDE) object and fills the object with data from the specified buffer. A DDE application uses this function during transactions that involve passing data to the partner application.

## -parameters

### -param idInst [in]

Type: <b>DWORD</b>

The application instance identifier obtained by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a> function.

### -param pSrc [in, optional]

Type: <b>LPBYTE</b>

The data to be copied to the DDE object. If this parameter is <b>NULL</b>, no data is copied to the object.

### -param cb [in]

Type: <b>DWORD</b>

The amount of memory, in bytes, to copy from the buffer pointed to by 
					<i>pSrc</i>. (include the terminating NULL, if the data is a string). If this parameter is zero, the 
					<i>pSrc</i> parameter is ignored.

### -param cbOff [in]

Type: <b>DWORD</b>

An offset, in bytes, from the beginning of the buffer pointed to by the 
					<i>pSrc</i> parameter. The data beginning at this offset is copied from the buffer to the DDE object.

### -param hszItem [in, optional]

Type: <b>HSZ</b>

A handle to the string that specifies the data item corresponding to the DDE object. This handle must have been created by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a> function. If the data handle is to be used in an <a href="/windows/desktop/dataxchg/xtyp-execute">XTYP_EXECUTE</a> transaction, this parameter must be 0L.

### -param wFmt [in]

Type: <b>UINT</b>

The standard clipboard format of the data.

### -param afCmd [in]

Type: <b>UINT</b>

The creation flags. This parameter can be <b>HDATA_APPOWNED</b>, which specifies that the server application calling the <b>DdeCreateDataHandle</b> function owns the data handle this function creates. This flag enables the application to share the data handle with other DDEML applications rather than creating a separate handle to pass to each application. If this flag is specified, the application must eventually free the shared memory object associated with the handle by using the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddefreedatahandle">DdeFreeDataHandle</a> function. If this flag is not specified, the handle becomes invalid in the application that created the handle after the data handle is returned by the application's DDE callback function or is used as a parameter in another DDEML function.

## -returns

Type: <b>HDDEDATA</b>

If the function succeeds, the return value is a data handle.

If the function fails, the return value is 0L. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

Any unfilled locations in the DDE object are undefined. 

After a data handle has been used as a parameter in another DDEML function or has been returned by a DDE callback function, the handle can be used only for read access to the DDE object identified by the handle.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeaccessdata">DdeAccessData</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatestringhandlea">DdeCreateStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddefreedatahandle">DdeFreeDataHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetdata">DdeGetData</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeinitializea">DdeInitialize</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>