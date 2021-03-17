---
UID: NF:ddeml.DdeQueryConvInfo
title: DdeQueryConvInfo function (ddeml.h)
description: Retrieves information about a Dynamic Data Exchange (DDE) transaction and about the conversation in which the transaction takes place.
helpviewer_keywords: ["DdeQueryConvInfo","DdeQueryConvInfo function [Data Exchange]","_win32_DdeQueryConvInfo","_win32_ddequeryconvinfo_cpp","dataxchg.ddequeryconvinfo","ddeml/DdeQueryConvInfo","winui._win32_ddequeryconvinfo"]
old-location: dataxchg\ddequeryconvinfo.htm
tech.root: dataxchg
ms.assetid: VS|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchangemanagementlibrary\dynamicdataexchangemanagementreference\dynamicdataexchangemanagementfunctions\ddequeryconvinfo.htm
ms.date: 12/05/2018
ms.keywords: DdeQueryConvInfo, DdeQueryConvInfo function [Data Exchange], _win32_DdeQueryConvInfo, _win32_ddequeryconvinfo_cpp, dataxchg.ddequeryconvinfo, ddeml/DdeQueryConvInfo, winui._win32_ddequeryconvinfo
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
 - DdeQueryConvInfo
 - ddeml/DdeQueryConvInfo
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
 - DdeQueryConvInfo
---

# DdeQueryConvInfo function


## -description

Retrieves information about a Dynamic Data Exchange (DDE) transaction and about the conversation in which the transaction takes place.

## -parameters

### -param hConv [in]

Type: <b>HCONV</b>

A handle to the conversation.

### -param idTransaction [in]

Type: <b>DWORD</b>

The transaction. For asynchronous transactions, this parameter should be a transaction identifier returned by the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddeclienttransaction">DdeClientTransaction</a> function. For synchronous transactions, this parameter should be QID_SYNC.

### -param pConvInfo [in, out]

Type: <b>PCONVINFO</b>

A pointer to the <a href="/windows/desktop/api/ddeml/ns-ddeml-convinfo">CONVINFO</a> structure that receives information about the transaction and conversation. The 
					<i>cb</i> member of the <b>CONVINFO</b> structure must specify the length of the buffer allocated for the structure.

## -returns

Type: <b>UINT</b>

If the function succeeds, the return value is the number of bytes copied into the <a href="/windows/desktop/api/ddeml/ns-ddeml-convinfo">CONVINFO</a> structure.

If the function fails, the return value is <b>FALSE</b>. 

The <a href="/windows/desktop/api/ddeml/nf-ddeml-ddegetlasterror">DdeGetLastError</a> function can be used to get the error code, which can be one of the following values:

## -remarks

An application should not free a string handle referenced by the <a href="/windows/desktop/api/ddeml/ns-ddeml-convinfo">CONVINFO</a> structure. If an application must use one of these string handles, it should call the <a href="/windows/desktop/api/ddeml/nf-ddeml-ddekeepstringhandle">DdeKeepStringHandle</a> function to create a copy of the handle. 

If the 
				<i>idTransaction</i> parameter is set to QID_SYNC, the 
				<i>hUser</i> member of the <a href="/windows/desktop/api/ddeml/ns-ddeml-convinfo">CONVINFO</a> structure is associated with the conversation and can be used to hold data associated with the conversation. If 
				<i>idTransaction</i> is the identifier of an asynchronous transaction, the 
				<i>hUser</i> member is associated only with the current transaction and is valid only for the duration of the transaction.

## -see-also

<a href="/windows/desktop/api/ddeml/ns-ddeml-convinfo">CONVINFO</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeclienttransaction">DdeClientTransaction</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnect">DdeConnect</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddeconnectlist">DdeConnectList</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddekeepstringhandle">DdeKeepStringHandle</a>



<a href="/windows/desktop/api/ddeml/nf-ddeml-ddequerynextserver">DdeQueryNextServer</a>



<a href="/windows/desktop/dataxchg/dynamic-data-exchange-management-library">Dynamic Data Exchange Management Library</a>



<b>Reference</b>