---
UID: NF:clfsmgmtw32.RemoveLogPolicy
title: RemoveLogPolicy function (clfsmgmtw32.h)
description: Resets the specified policy to its default behavior.
helpviewer_keywords: ["RemoveLogPolicy","RemoveLogPolicy function [Files]","clfsmgmtw32/RemoveLogPolicy","fs.removelogpolicy"]
old-location: fs\removelogpolicy.htm
tech.root: fs
ms.assetid: 06e8c1bf-f190-4f3d-a588-5c8dd2e99f43
ms.date: 12/05/2018
ms.keywords: RemoveLogPolicy, RemoveLogPolicy function [Files], clfsmgmtw32/RemoveLogPolicy, fs.removelogpolicy
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
 - RemoveLogPolicy
 - clfsmgmtw32/RemoveLogPolicy
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
 - RemoveLogPolicy
---

# RemoveLogPolicy function


## -description

Resets the specified policy to its default behavior.

## -parameters

### -param hLog [in]

Handle to the log to reset the policy for.

### -param ePolicyType [in]

Specifies the policy to reset. Policy types are enumerated in <a href="/windows/desktop/api/clfsmgmt/ne-clfsmgmt-clfs_mgmt_policy_type">CLFS_MGMT_POLICY_TYPE</a>.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/clfsmgmt/ns-clfsmgmt-clfs_mgmt_policy">CLFS_MGMT_POLICY</a>



<a href="/windows/desktop/api/clfsmgmt/ne-clfsmgmt-clfs_mgmt_policy_type">CLFS_MGMT_POLICY_TYPE</a>



<a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-querylogpolicy">QueryLogPolicy</a>