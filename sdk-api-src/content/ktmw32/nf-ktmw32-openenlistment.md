---
UID: NF:ktmw32.OpenEnlistment
title: OpenEnlistment function (ktmw32.h)
description: Opens an existing enlistment object, and returns a handle to the enlistment.
helpviewer_keywords: ["OpenEnlistment","OpenEnlistment function [Files]","fs.openenlistment","ktmw32/OpenEnlistment"]
old-location: fs\openenlistment.htm
tech.root: fs
ms.assetid: 2c403e22-3feb-415a-b65b-572802764548
ms.date: 12/05/2018
ms.keywords: OpenEnlistment, OpenEnlistment function [Files], fs.openenlistment, ktmw32/OpenEnlistment
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
 - OpenEnlistment
 - ktmw32/OpenEnlistment
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
 - OpenEnlistment
---

# OpenEnlistment function


## -description

Opens an existing enlistment object, and returns a handle to the enlistment.

## -parameters

### -param dwDesiredAccess [in]

The access requested for this enlistment. See <a href="/windows/desktop/Ktm/enlistment-access-masks">Enlistment Access Masks</a> for a list of valid values.

### -param ResourceManagerHandle [in]

A handle to the resource manager.

### -param EnlistmentId [in]

The enlistment identifier.

## -returns

If the function succeeds, the return value is a handle to the enlistment.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the  possible error codes:

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createenlistment">CreateEnlistment</a>



<a href="/windows/desktop/Ktm/enlistment-access-masks">Enlistment Access Masks</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>