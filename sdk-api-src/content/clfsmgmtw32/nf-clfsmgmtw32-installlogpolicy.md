---
UID: NF:clfsmgmtw32.InstallLogPolicy
title: InstallLogPolicy function
author: windows-driver-content
description: Installs (sets) a policy for a log.
old-location: fs\installlogpolicy.htm
old-project: Clfs
ms.assetid: c397e506-b7a9-4189-bf1b-6df81db8e187
ms.author: windowsdriverdev
ms.date: 5/10/2018
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
req.typenames: CLFS_MGMT_POLICY, *PCLFS_MGMT_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	InstallLogPolicy
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# InstallLogPolicy function


## -description


Installs (sets) a policy for a log.


## -parameters




### -param hLog [in]

A handle to a log.


### -param pPolicy [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541842">CLFS_MGMT_POLICY</a> structure that represents the desired policy to install.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541842">CLFS_MGMT_POLICY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541849">CLFS_MGMT_POLICY_TYPE</a>



<a href="https://msdn.microsoft.com/4da401cf-3606-4ae1-ae6f-37eb3dea6426">SetLogFileSizeWithPolicy</a>
 

 

