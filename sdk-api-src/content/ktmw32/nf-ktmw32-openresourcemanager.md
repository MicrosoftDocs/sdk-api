---
UID: NF:ktmw32.OpenResourceManager
title: OpenResourceManager function (ktmw32.h)
description: Opens an existing resource manager (RM).
helpviewer_keywords: ["OpenResourceManager","OpenResourceManager function [Files]","fs.openresourcemanager","ktmw32/OpenResourceManager"]
old-location: fs\openresourcemanager.htm
tech.root: fs
ms.assetid: 396b586f-c594-4481-b095-862e9058519c
ms.date: 12/05/2018
ms.keywords: OpenResourceManager, OpenResourceManager function [Files], fs.openresourcemanager, ktmw32/OpenResourceManager
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
 - OpenResourceManager
 - ktmw32/OpenResourceManager
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
 - OpenResourceManager
---

# OpenResourceManager function


## -description

Opens an existing resource manager (RM).

## -parameters

### -param dwDesiredAccess [in]

The access requested for the RM. See <a href="/windows/desktop/Ktm/resource-manager-access-masks">Resource Manager Access Masks</a> for a list of valid values.

### -param TmHandle [in]

A handle to the transaction manager.

### -param ResourceManagerId [in]

The identifier  for this resource manager.

## -returns

If the function succeeds, the return value is a handle to the resource manager.

If the function fails, the return value is INVALID_HANDLE_VALUE. To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

The following list identifies the  possible error codes:

## -remarks

Immediately after calling this function, you must call <a href="/windows/desktop/api/ktmw32/nf-ktmw32-recoverresourcemanager">RecoverResourceManager</a>.

## -see-also

<a href="/windows/desktop/api/ktmw32/nf-ktmw32-createresourcemanager">CreateResourceManager</a>



<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>



<a href="/windows/desktop/Ktm/resource-manager-access-masks">Resource Manager Access Masks</a>