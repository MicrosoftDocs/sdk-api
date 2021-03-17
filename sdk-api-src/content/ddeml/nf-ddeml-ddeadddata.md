---
UID: NF:ddeml.DdeAddData
title: DdeAddData function (ddeml.h)
description: Adds data to the specified Dynamic Data Exchange (DDE) object.
helpviewer_keywords: ["DdeAddData","DdeAddData function [Data Exchange]","_win32_DdeAddData","_win32_ddeadddata_cpp","dataxchg.ddeadddata","ddeml/DdeAddData","winui._win32_ddeadddata"]
old-location: dataxchg\ddeadddata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeadddata.htm
ms.date: 12/05/2018
ms.keywords: DdeAddData, DdeAddData function [Data Exchange], _win32_DdeAddData, _win32_ddeadddata_cpp, dataxchg.ddeadddata, ddeml/DdeAddData, winui._win32_ddeadddata
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
 - DdeAddData
 - ddeml/DdeAddData
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
 - DdeAddData
---

# DdeAddData function


## -description

Adds data to the specified Dynamic Data Exchange (DDE) object. An application can add data starting at any offset from the beginning of the object. If new data overlaps data already in the object, the new data overwrites the old data in the bytes where the overlap occurs. The contents of locations in the object that have not been written to are undefined.

## -parameters

### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object that receives additional data.

### -param pSrc [in]

Type: <b>LPBYTE</b>

The data to be added to the DDE object.

### -param cb [in]

Type: <b>DWORD</b>

The length, in bytes, of the data to be added to the DDE object, including the terminating <b>NULL</b>, if the data is a string.

### -param cbOff [in]

Type: <b>DWORD</b>

An offset, in bytes, from the beginning of the DDE object. The additional data is copied to the object beginning at this offset.

## -returns

Type: <b>HDDEDATA</b>

If the function succeeds, the return value is a new handle to the DDE object. The new handle is used in all references to the object. 

If the function fails, the return value is zero. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

After a data handle has been used as a parameter in another <a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a> function or has been returned by a DDE callback function, the handle can be used only for read access to the DDE object identified by the handle. 

If the amount of memory originally allocated is less than is needed to hold the added data, <b>DdeAddData</b> reallocates a global memory object of the appropriate size.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeaccessdata">DdeAccessData</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatedatahandle">DdeCreateDataHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeunaccessdata">DdeUnaccessData</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>