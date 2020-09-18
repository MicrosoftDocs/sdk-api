---
UID: NF:ktmw32.RecoverEnlistment
title: RecoverEnlistment function (ktmw32.h)
description: Recovers an enlistment's state.
helpviewer_keywords: ["RecoverEnlistment","RecoverEnlistment function [Files]","fs.recoverenlistment","ktmw32/RecoverEnlistment"]
old-location: fs\recoverenlistment.htm
tech.root: fs
ms.assetid: 5c36732f-bf4f-4071-959e-3359be0b2363
ms.date: 12/05/2018
ms.keywords: RecoverEnlistment, RecoverEnlistment function [Files], fs.recoverenlistment, ktmw32/RecoverEnlistment
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
 - RecoverEnlistment
 - ktmw32/RecoverEnlistment
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
 - RecoverEnlistment
---

# RecoverEnlistment function


## -description

Recovers an enlistment's state.

## -parameters

### -param EnlistmentHandle [in]

A handle to the enlistment.

### -param EnlistmentKey [in, optional]

The key to the enlistment to be recovered.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>