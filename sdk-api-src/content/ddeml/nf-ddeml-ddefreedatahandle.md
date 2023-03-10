---
UID: NF:ddeml.DdeFreeDataHandle
title: DdeFreeDataHandle function (ddeml.h)
description: Frees a Dynamic Data Exchange (DDE) object and deletes the data handle associated with the object.
helpviewer_keywords: ["DdeFreeDataHandle","DdeFreeDataHandle function [Data Exchange]","_win32_DdeFreeDataHandle","_win32_ddefreedatahandle_cpp","dataxchg.ddefreedatahandle","ddeml/DdeFreeDataHandle","winui._win32_ddefreedatahandle"]
old-location: dataxchg\ddefreedatahandle.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddefreedatahandle.htm
ms.date: 12/05/2018
ms.keywords: DdeFreeDataHandle, DdeFreeDataHandle function [Data Exchange], _win32_DdeFreeDataHandle, _win32_ddefreedatahandle_cpp, dataxchg.ddefreedatahandle, ddeml/DdeFreeDataHandle, winui._win32_ddefreedatahandle
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
 - DdeFreeDataHandle
 - ddeml/DdeFreeDataHandle
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
 - DdeFreeDataHandle
---

# DdeFreeDataHandle function


## -description

Frees a Dynamic Data Exchange (DDE) object and deletes the data handle associated with the object.

## -parameters

### -param hData [in]

Type: <b>HDDEDATA</b>

A handle to the DDE object to be freed. This handle must have been created by a previous call to the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatedatahandle">DdeCreateDataHandle</a> function or returned by the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeclienttransaction">DdeClientTransaction</a> function.

## -returns

Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

An application must call <b>DdeFreeDataHandle</b> under the following circumstances: 

<ul>
<li>To free a DDE object that the application allocated by calling the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatedatahandle">DdeCreateDataHandle</a> function if the object's data handle was never passed by the application to another Dynamic Data Exchange Management Library (DDEML) function </li>
<li>To free a DDE object that the application allocated by specifying the <b>HDATA_APPOWNED</b> flag in a call to <a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatedatahandle">DdeCreateDataHandle</a>
</li>
<li>To free a DDE object whose handle the application received from the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeclienttransaction">DdeClientTransaction</a> function </li>
</ul>
The system automatically frees an unowned object when its handle is returned by a DDE callback function or is used as a parameter in a DDEML function.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeaccessdata">DdeAccessData</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeclienttransaction">DdeClientTransaction</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddecreatedatahandle">DdeCreateDataHandle</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>