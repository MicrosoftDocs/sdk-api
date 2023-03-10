---
UID: NF:ktmw32.RecoverResourceManager
title: RecoverResourceManager function (ktmw32.h)
description: Recovers a resource manager's state from its log file.
helpviewer_keywords: ["RecoverResourceManager","RecoverResourceManager function [Files]","fs.recoverresourcemanager","ktmw32/RecoverResourceManager"]
old-location: fs\recoverresourcemanager.htm
tech.root: fs
ms.assetid: 616ff873-c0d0-464e-9b1b-74a426b99abd
ms.date: 12/05/2018
ms.keywords: RecoverResourceManager, RecoverResourceManager function [Files], fs.recoverresourcemanager, ktmw32/RecoverResourceManager
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
 - RecoverResourceManager
 - ktmw32/RecoverResourceManager
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
 - RecoverResourceManager
---

# RecoverResourceManager function


## -description

Recovers a resource manager's state from its log file.

## -parameters

### -param ResourceManagerHandle [in]

A handle to the resource manager.

## -returns

If the function succeeds, the return value is nonzero. 


  

If the function fails, the return value is zero (0). To get extended error information, call the <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function.

 The following list identifies the possible error codes:

## -see-also

<a href="/windows/desktop/Ktm/kernel-transaction-manager-functions">Kernel Transaction Manager Functions</a>