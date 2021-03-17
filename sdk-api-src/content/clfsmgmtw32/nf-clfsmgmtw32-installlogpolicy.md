---
UID: NF:clfsmgmtw32.InstallLogPolicy
title: InstallLogPolicy function (clfsmgmtw32.h)
description: Installs (sets) a policy for a log.
helpviewer_keywords: ["InstallLogPolicy","InstallLogPolicy function [Files]","clfsmgmtw32/InstallLogPolicy","fs.installlogpolicy"]
old-location: fs\installlogpolicy.htm
tech.root: fs
ms.assetid: c397e506-b7a9-4189-bf1b-6df81db8e187
ms.date: 12/05/2018
ms.keywords: InstallLogPolicy, InstallLogPolicy function [Files], clfsmgmtw32/InstallLogPolicy, fs.installlogpolicy
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
 - InstallLogPolicy
 - clfsmgmtw32/InstallLogPolicy
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
 - InstallLogPolicy
---

# InstallLogPolicy function


## -description

Installs (sets) a policy for a log.

## -parameters

### -param hLog [in]

A handle to a log.

### -param pPolicy [in]

A pointer to a <a href="/windows/desktop/api/clfsmgmt/ns-clfsmgmt-clfs_mgmt_policy">CLFS_MGMT_POLICY</a> structure that represents the desired policy to install.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

Installing a log policy does not trigger an immediate change in behavior.


#### Examples

For an example that uses this function, see <a href="/previous-versions/windows/desktop/clfs/creating-a-log-file">Creating a Log File</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/clfsmgmt/ns-clfsmgmt-clfs_mgmt_policy">CLFS_MGMT_POLICY</a>



<a href="/windows/desktop/api/clfsmgmt/ne-clfsmgmt-clfs_mgmt_policy_type">CLFS_MGMT_POLICY_TYPE</a>



<a href="/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-setlogfilesizewithpolicy">SetLogFileSizeWithPolicy</a>