---
UID: NF:ddeml.DdeUnaccessData
title: DdeUnaccessData function (ddeml.h)
description: Unaccesses a Dynamic Data Exchange (DDE) object. An application must call this function after it has finished accessing the object.
helpviewer_keywords: ["DdeUnaccessData","DdeUnaccessData function [Data Exchange]","_win32_DdeUnaccessData","_win32_ddeunaccessdata_cpp","dataxchg.ddeunaccessdata","ddeml/DdeUnaccessData","winui._win32_ddeunaccessdata"]
old-location: dataxchg\ddeunaccessdata.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddeunaccessdata.htm
ms.date: 12/05/2018
ms.keywords: DdeUnaccessData, DdeUnaccessData function [Data Exchange], _win32_DdeUnaccessData, _win32_ddeunaccessdata_cpp, dataxchg.ddeunaccessdata, ddeml/DdeUnaccessData, winui._win32_ddeunaccessdata
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
 - DdeUnaccessData
 - ddeml/DdeUnaccessData
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
 - DdeUnaccessData
---

# DdeUnaccessData function


## -description

Unaccesses a Dynamic Data Exchange (DDE) object. An application must call this function after it has finished accessing the object.

## -parameters

### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeaccessdata">DdeAccessData</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeadddata">DdeAddData</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatedatahandle">DdeCreateDataHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddefreedatahandle">DdeFreeDataHandle</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>