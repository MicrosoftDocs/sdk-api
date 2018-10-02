---
UID: NF:clfsmgmtw32.InstallLogPolicy
title: InstallLogPolicy function
author: windows-sdk-content
description: Installs (sets) a policy for a log.
old-location: fs\installlogpolicy.htm
tech.root: Clfs
ms.assetid: c397e506-b7a9-4189-bf1b-6df81db8e187
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: InstallLogPolicy, InstallLogPolicy function [Files], clfsmgmtw32/InstallLogPolicy, fs.installlogpolicy
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
---

# InstallLogPolicy function


## -description


Installs (sets) a policy for a log.


## -parameters




### -param hLog [in]

A handle to a log.


### -param pPolicy [in]

A pointer to a <a href="https://msdn.microsoft.com/3f5d9c38-b299-4102-9786-115ece5b0928">CLFS_MGMT_POLICY</a> structure that represents the desired policy to install.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



Installing a log policy does not trigger an immediate change in behavior.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/70d1f73b-bb39-46f8-a2fa-e68693a56082">Creating a Log File</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/3f5d9c38-b299-4102-9786-115ece5b0928">CLFS_MGMT_POLICY</a>



<a href="https://msdn.microsoft.com/eaa817be-04ac-48c2-b7de-60509b1f65c7">CLFS_MGMT_POLICY_TYPE</a>



<a href="https://msdn.microsoft.com/4da401cf-3606-4ae1-ae6f-37eb3dea6426">SetLogFileSizeWithPolicy</a>
 

 

