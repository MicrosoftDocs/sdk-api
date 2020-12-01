---
UID: NF:tspi.TSPI_lineUncompleteCall
title: TSPI_lineUncompleteCall function (tspi.h)
description: The TSPI_lineUncompleteCall function is used to cancel the specified call completion request on the specified line.
helpviewer_keywords: ["TSPI_lineUncompleteCall","TSPI_lineUncompleteCall function [TAPI 2.2]","_tspi_tspi_lineuncompletecall","tspi.tspi_lineuncompletecall","tspi/TSPI_lineUncompleteCall"]
old-location: tspi\tspi_lineuncompletecall.htm
tech.root: tapi3
ms.assetid: e8b5ee74-245f-4d91-8996-eec482241e4d
ms.date: 12/05/2018
ms.keywords: TSPI_lineUncompleteCall, TSPI_lineUncompleteCall function [TAPI 2.2], _tspi_tspi_lineuncompletecall, tspi.tspi_lineuncompletecall, tspi/TSPI_lineUncompleteCall
req.header: tspi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TSPI_lineUncompleteCall
 - tspi/TSPI_lineUncompleteCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Tspi.h
api_name:
 - TSPI_lineUncompleteCall
---

# TSPI_lineUncompleteCall function


## -description

The 
<b>TSPI_lineUncompleteCall</b> function is used to cancel the specified call completion request on the specified line.

## -parameters

### -param dwRequestID

The identifier of the asynchronous request.

### -param hdLine

The handle to the line on which a call completion is to be canceled.

### -param dwCompletionID

The completion identifier for the request that is to be canceled. TAPI does not validate this parameter when this function is called.

## -returns

Returns <i>dwRequestID</i>, or an error number if an error occurs. The <i>lResult</i> actual parameter of the corresponding 
<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a> is zero if the function succeeds, or an error number if an error occurs. Possible return values are as follows:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONUNAVAIL, LINEERR_INVALCOMPLETIONID, LINEERR_OPERATIONFAILED, LINEERR_NOMEM, LINEERR_RESOURCEUNAVAIL.

## -see-also

<a href="/windows/desktop/api/tspi/nc-tspi-async_completion">ASYNC_COMPLETION</a>



<a href="/windows/desktop/api/tspi/nf-tspi-tspi_linecompletecall">TSPI_lineCompleteCall</a>