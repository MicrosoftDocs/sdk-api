---
UID: NF:clfsw32.AdvanceLogBase
title: AdvanceLogBase function (clfsw32.h)
description: Advances the base log sequence number (LSN) of a log stream to the specified LSN.
helpviewer_keywords: ["AdvanceLogBase","AdvanceLogBase function [Files]","clfsw32/AdvanceLogBase","fs.advancelogbase"]
old-location: fs\advancelogbase.htm
tech.root: fs
ms.assetid: aecdea3b-ac42-43d4-88b3-14cd810a4017
ms.date: 12/05/2018
ms.keywords: AdvanceLogBase, AdvanceLogBase function [Files], clfsw32/AdvanceLogBase, fs.advancelogbase
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AdvanceLogBase
 - clfsw32/AdvanceLogBase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - AdvanceLogBase
---

# AdvanceLogBase function


## -description

 Advances the base log sequence number (LSN) of a log stream to the   specified LSN.

## -parameters

### -param pvMarshal [in, out]

A pointer to the marshaling context  that  a successful call to  <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> returns.

### -param plsnBase [in]

The new base LSN for the log that is specified in <i>pvMarshal</i>.  

This LSN must be in the range between the current base LSN and the last LSN of the log, inclusively.

### -param fFlags [in]

This parameter is not implemented at this time, and must be zero.

### -param pOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that is required for asynchronous operation. 

If asynchronous operation is not used, this parameter can be <b>NULL</b>.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following list identifies the possible error codes:

## -remarks

<b>AdvanceLogBase</b> might flush data and metadata when it is called.

## -see-also

<a href="/previous-versions/windows/desktop/clfs/obtaining-the-next-lsn">Obtaining the Next LSN</a>