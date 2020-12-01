---
UID: NF:ddeml.DdeAccessData
title: DdeAccessData function (ddeml.h)
description: Provides access to the data in the specified Dynamic Data Exchange (DDE) object. An application must call the DdeUnaccessData function when it has finished accessing the data in the object.
helpviewer_keywords: ["DdeAccessData","DdeAccessData function [Data Exchange]","_win32_DdeAccessData","_win32_ddeaccessdata_cpp","dataxchg.ddeaccessdata","ddeml/DdeAccessData","winui._win32_ddeaccessdata"]
old-location: dataxchg\ddeaccessdata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeaccessdata.htm
ms.date: 12/05/2018
ms.keywords: DdeAccessData, DdeAccessData function [Data Exchange], _win32_DdeAccessData, _win32_ddeaccessdata_cpp, dataxchg.ddeaccessdata, ddeml/DdeAccessData, winui._win32_ddeaccessdata
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
 - DdeAccessData
 - ddeml/DdeAccessData
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
 - DdeAccessData
---

# DdeAccessData function


## -description

Provides access to the data in the specified Dynamic Data Exchange (DDE) object. An application must call the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeunaccessdata">DdeUnaccessData</a> function when it has finished accessing the data in the object.

## -parameters

### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object to be accessed.

### -param pcbDataSize [out, optional]

Type: <b>LPDWORD</b>

A pointer to a variable that receives the size, in bytes, of the DDE object identified by the 
					<i>hData</i> parameter. If this parameter is <b>NULL</b>, no size information is returned.

## -returns

Type: <b>LPBYTE</b>

If the function succeeds, the return value is a pointer to the first byte of data in the DDE object.

If the function fails, the return value is <b>NULL</b>. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

If the 
				<i>hData</i> parameter has not been passed to a Dynamic Data Exchange Management Library (DDEML) function, an application can use the pointer returned by <b>DdeAccessData</b> for read-write access to the DDE object. If 
				<i>hData</i> has already been passed to a DDEML function, the pointer should be used only for read access to the memory object.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeadddata">DdeAddData</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatedatahandle">DdeCreateDataHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddefreedatahandle">DdeFreeDataHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeunaccessdata">DdeUnaccessData</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>