---
UID: NF:clfsmgmtw32.RemoveLogPolicy
title: RemoveLogPolicy function
author: windows-driver-content
description: Resets the specified policy to its default behavior.
old-location: fs\removelogpolicy.htm
old-project: Clfs
ms.assetid: 06e8c1bf-f190-4f3d-a588-5c8dd2e99f43
ms.author: windowsdriverdev
ms.date: 4/25/2018
ms.keywords: RemoveLogPolicy, RemoveLogPolicy function [Files], clfsmgmtw32/RemoveLogPolicy, fs.removelogpolicy
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
-	RemoveLogPolicy
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# RemoveLogPolicy function


## -description


Resets the specified policy to its default behavior.


## -parameters




### -param hLog [in]

Handle to the log to reset the policy for.


### -param ePolicyType [in]

Specifies the policy to reset. Policy types are enumerated in <a href="https://msdn.microsoft.com/library/windows/hardware/ff541849">CLFS_MGMT_POLICY_TYPE</a>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero (0). To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541842">CLFS_MGMT_POLICY</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541849">CLFS_MGMT_POLICY_TYPE</a>



<a href="https://msdn.microsoft.com/45bed7c7-132e-48f9-8b9a-d8cb1580f456">QueryLogPolicy</a>
 

 

