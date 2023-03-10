---
UID: NF:tapi.lineUncompleteCall
title: lineUncompleteCall function (tapi.h)
description: The lineUncompleteCall function cancels the specified call completion request on the specified line.
helpviewer_keywords: ["_tapi2_lineuncompletecall","lineUncompleteCall","lineUncompleteCall function [TAPI 2.2]","tapi/lineUncompleteCall","tapi2.lineuncompletecall"]
old-location: tapi2\lineuncompletecall.htm
tech.root: tapi3
ms.assetid: e6b87d84-071c-4b75-afbf-569a5a861e3a
ms.date: 12/05/2018
ms.keywords: _tapi2_lineuncompletecall, lineUncompleteCall, lineUncompleteCall function [TAPI 2.2], tapi/lineUncompleteCall, tapi2.lineuncompletecall
req.header: tapi.h
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
req.lib: Tapi32.lib
req.dll: Tapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineUncompleteCall
 - tapi/lineUncompleteCall
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tapi32.dll
api_name:
 - lineUncompleteCall
---

# lineUncompleteCall function


## -description

The 
<b>lineUncompleteCall</b> function cancels the specified call completion request on the specified line.

## -parameters

### -param hLine

Handle to the line device on which a call completion is to be canceled.

### -param dwCompletionID

Completion identifier for the request that is to be canceled.

## -returns

Returns a positive request identifier if the function is completed asynchronously, or a negative error number if an error occurs. The <i>dwParam2</i> parameter of the corresponding 
<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a> message is zero if the function succeeds or it is a negative error number if an error occurs. Possible return values are:

LINEERR_INVALLINEHANDLE, LINEERR_OPERATIONFAILED, LINEERR_INVALCOMPLETIONID, LINEERR_RESOURCEUNAVAIL, LINEERR_NOMEM, LINEERR_UNINITIALIZED, LINEERR_OPERATIONUNAVAIL.

## -see-also

<a href="/windows/desktop/Tapi/line-reply">LINE_REPLY</a>



<a href="/windows/desktop/Tapi/supplementary-line-service-functions">Supplementary Line Service Functions</a>



<a href="/windows/desktop/Tapi/tapi-2-2-reference">TAPI 2.2 Reference Overview</a>