---
UID: NF:securitybaseapi.CheckTokenCapability
title: CheckTokenCapability function
author: windows-sdk-content
description: Checks the capabilities of a given token.
old-location: security\checktokencapability.htm
old-project: SecAuthZ
ms.assetid: 436A5110-B79E-4E64-92E8-1C9E713D0948
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CheckTokenCapability, CheckTokenCapability function [Security], security.checktokencapability, securitybaseapi/CheckTokenCapability
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: securitybaseapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: EXTENDED_NAME_FORMAT, *PEXTENDED_NAME_FORMAT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Security-base-l1-2-0.dll
 - KernelBase.dll
 - MinKernelBase.dll
 - API-MS-Win-Security-Base-L1-2-1.dll
api_name:
 - CheckTokenCapability
product: Windows
targetos: Windows
req.lib: 
req.dll: Kernel32.dll
req.irql: 
req.product: ADAM
---

# CheckTokenCapability function


## -description


The <b>CheckTokenCapability</b> function checks the capabilities of a given token.


## -parameters




### -param TokenHandle [in, optional]

A handle to an access token. The handle must have TOKEN_QUERY access to the token. The token must be an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>. 
      

If <i>TokenHandle</i> is <b>NULL</b>, <b>CheckTokenCapability</b> uses the impersonation token of the calling thread. If the thread is not impersonating, the function duplicates the thread's <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">primary token</a> to create an <a href="https://msdn.microsoft.com/af511aed-88f5-4b12-ad44-317925297f70">impersonation token</a>.


### -param CapabilitySidToCheck [in]

A pointer to a capability <a href="https://msdn.microsoft.com/library/windows/hardware/ff556740">SID</a> structure. The <b>CheckTokenCapability</b> function checks the capabilities of this access token.


### -param HasCapability [out]

Receives the results of the check. If the access token has the capability, it returns <b>TRUE</b>, otherwise, it returns <b>FALSE</b>.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>




