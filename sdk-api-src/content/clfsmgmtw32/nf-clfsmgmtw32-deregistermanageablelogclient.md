---
UID: NF:clfsmgmtw32.DeregisterManageableLogClient
title: DeregisterManageableLogClient function (clfsmgmtw32.h)
description: Deregisters a client with the log manager.
helpviewer_keywords: ["DeregisterManageableLogClient","DeregisterManageableLogClient function [Files]","clfsmgmtw32/DeregisterManageableLogClient","fs.deregistermanageablelogclient"]
old-location: fs\deregistermanageablelogclient.htm
tech.root: fs
ms.assetid: 293a4856-62d4-49a3-9177-4d09a0897200
ms.date: 12/05/2018
ms.keywords: DeregisterManageableLogClient, DeregisterManageableLogClient function [Files], clfsmgmtw32/DeregisterManageableLogClient, fs.deregistermanageablelogclient
req.header: clfsmgmtw32.h
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
 - DeregisterManageableLogClient
 - clfsmgmtw32/DeregisterManageableLogClient
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
 - DeregisterManageableLogClient
---

# DeregisterManageableLogClient function


## -description

The <b>DeregisterManageableLogClient</b> function deregisters a client with the log manager.

## -parameters

### -param hLog [in]

The handle to deregister.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-registermanageablelogclient">RegisterManageableLogClient</a>