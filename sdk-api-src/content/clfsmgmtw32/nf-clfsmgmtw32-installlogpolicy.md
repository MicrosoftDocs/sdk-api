---
UID: NF:clfsmgmtw32.InstallLogPolicy
title: InstallLogPolicy function (clfsmgmtw32.h)
author: windows-sdk-content
description: Installs (sets) a policy for a log.
old-location: fs\installlogpolicy.htm
tech.root: Clfs
ms.assetid: c397e506-b7a9-4189-bf1b-6df81db8e187
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InstallLogPolicy, InstallLogPolicy function [Files], clfsmgmtw32/InstallLogPolicy, fs.installlogpolicy
ms.topic: function
f1_keywords: 
 - "clfsmgmtw32/InstallLogPolicy"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - InstallLogPolicy
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# InstallLogPolicy function


## -description


Installs (sets) a policy for a log.


## -parameters




### -param hLog [in]

A handle to a log.


### -param pPolicy [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/clfsmgmt/ns-clfsmgmt-_clfs_mgmt_policy">CLFS_MGMT_POLICY</a> structure that represents the desired policy to install.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -remarks



Installing a log policy does not trigger an immediate change in behavior.


#### Examples

For an example that uses this function, see <a href="https://docs.microsoft.com/previous-versions/windows/desktop/clfs/creating-a-log-file">Creating a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/clfsmgmt/ns-clfsmgmt-_clfs_mgmt_policy">CLFS_MGMT_POLICY</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfsmgmt/ne-clfsmgmt-_clfs_mgmt_policy_type">CLFS_MGMT_POLICY_TYPE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/clfsmgmtw32/nf-clfsmgmtw32-setlogfilesizewithpolicy">SetLogFileSizeWithPolicy</a>
 

 

