---
UID: NF:clfsmgmtw32.QueryLogPolicy
title: QueryLogPolicy function (clfsmgmtw32.h)
description: The QueryLogPolicy function allows you to obtain a policy that is installed for the specified log.
helpviewer_keywords: ["QueryLogPolicy","QueryLogPolicy function [Files]","clfsmgmtw32/QueryLogPolicy","fs.querylogpolicy"]
old-location: fs\querylogpolicy.htm
tech.root: fs
ms.assetid: 45bed7c7-132e-48f9-8b9a-d8cb1580f456
ms.date: 12/05/2018
ms.keywords: QueryLogPolicy, QueryLogPolicy function [Files], clfsmgmtw32/QueryLogPolicy, fs.querylogpolicy
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
 - QueryLogPolicy
 - clfsmgmtw32/QueryLogPolicy
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
 - QueryLogPolicy
---

# QueryLogPolicy function


## -description

The <b>QueryLogPolicy</b> function allows you to obtain a policy that is installed for the specified log.

## -parameters

### -param hLog [in]

The handle to the log to query.

### -param ePolicyType [in]

Specifies the type of policy to query for. Policy types are enumerated in <a href="/windows/desktop/api/clfsmgmt/ne-clfsmgmt-clfs_mgmt_policy_type">CLFS_MGMT_POLICY_TYPE</a>.

### -param pPolicyBuffer [out]

A pointer to a buffer to receive the returned policies.

### -param pcbPolicyBuffer [in, out]

A pointer to the size of <i>pPolicyBuffer</i>. If the buffer is not large enough, <i>pcbPolicyBuffer</i> receives the size buffer required to successfully retrieve the specified policies.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/clfsmgmt/ns-clfsmgmt-clfs_mgmt_policy">CLFS_MGMT_POLICY</a>



<a href="/windows/desktop/api/clfsmgmt/ne-clfsmgmt-clfs_mgmt_policy_type">CLFS_MGMT_POLICY_TYPE</a>



<a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-removelogpolicy">RemoveLogPolicy</a>