---
UID: NF:filehc.FindSyncContextFromName
title: FindSyncContextFromName function (filehc.h)
description: Retrieves the FIO_CONTEXT structure that is associated with the specified user name.
helpviewer_keywords: ["FindSyncContextFromName","FindSyncContextFromName function [Windows API]","filehc/FindSyncContextFromName","winprog._findsynccontextfromname"]
old-location: winprog\_findsynccontextfromname.htm
tech.root: winprog
ms.assetid: 1528b545-6d04-4315-a0ca-cebef6144fe9
ms.date: 12/05/2018
ms.keywords: FindSyncContextFromName, FindSyncContextFromName function [Windows API], filehc/FindSyncContextFromName, winprog._findsynccontextfromname
req.header: filehc.h
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
req.lib: Fcachdll.lib
req.dll: Fcachdll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FindSyncContextFromName
 - filehc/FindSyncContextFromName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Fcachdll.dll
api_name:
 - FindSyncContextFromName
---

# FindSyncContextFromName function


## -description

Retrieves the <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure that is associated with the specified user name.

## -parameters

### -param pNameCache [in]

A pointer to the name cache that the client is to use.

### -param lpbName [in]

A pointer to the name of the cached item.

### -param cbName [in]

The size, in bytes, of the value in <i>lpbName</i>.

### -param pfnCallback [in]

A pointer to a <a href="/previous-versions/bb432262(v=vs.85)">FCACHE_READ_CALLBACK</a> function.

<div class="alert"><b>Note</b>  If this parameter is <b>NULL</b>, no callback function is called.</div>
<div> </div>

### -param lpvClientContext [in]

A pointer to the context that is associated with the client. This context is passed to the callback function.

### -param hToken [in]

Request the cache to evaluate the embedded security descriptor. If <i>hToken</i> is zero, it is ignored.

### -param accessMask [in]

The security descriptor data. For more information, see <a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>.

### -param ppContext [out]

A pointer to a pointer to the <a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a> structure that is associated with the user name.

If the function returns <b>TRUE</b>, this parameter can return a <b>NULL</b> pointer. This occurs when the user passes a <b>NULL</b> FIO_CONTEXT to <a href="/windows/desktop/api/filehc/nf-filehc-associatecontextwithname">_AssociateContextWithName</a>.

## -returns

Returns <b>TRUE</b> if the name is found in the cache; otherwise, it returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/SecAuthZ/access-mask">ACCESS_MASK</a>



<a href="/windows/desktop/api/filehc/nf-filehc-associatecontextwithname">AssociateContextWithName</a>



<a href="/previous-versions/bb432262(v=vs.85)">FCACHE_READ_CALLBACK</a>



<a href="/previous-versions/exchange-server/exchange-10/ms528326(v=exchg.10)">FIO_CONTEXT</a>