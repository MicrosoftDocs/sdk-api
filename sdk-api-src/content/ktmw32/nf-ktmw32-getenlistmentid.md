---
UID: NF:ktmw32.GetEnlistmentId
title: GetEnlistmentId function (ktmw32.h)
description: Obtains the identifier (ID) for the specified enlistment.
helpviewer_keywords: ["GetEnlistmentId","GetEnlistmentId function [Files]","fs.getenlistmentid","ktmw32/GetEnlistmentId"]
old-location: fs\getenlistmentid.htm
tech.root: fs
ms.assetid: ffd37a2e-6bac-4566-bb15-eafce8a11c3b
ms.date: 12/05/2018
ms.keywords: GetEnlistmentId, GetEnlistmentId function [Files], fs.getenlistmentid, ktmw32/GetEnlistmentId
req.header: ktmw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ktmw32.lib
req.dll: Ktmw32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetEnlistmentId
 - ktmw32/GetEnlistmentId
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ktmw32.dll
api_name:
 - GetEnlistmentId
---

# GetEnlistmentId function


## -description

Obtains the identifier (ID) for the specified enlistment.

## -parameters

### -param EnlistmentHandle [in]

A handle to the enlistment.

### -param EnlistmentId [out]

A pointer to a variables that receives the ID of the enlistment.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is 0 (zero). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.


The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>