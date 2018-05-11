---
UID: NC:ntsecpkg.LSA_CLIENT_CALLBACK
title: LSA_CLIENT_CALLBACK
author: windows-driver-content
description: Allows a Local Security Authority (LSA)-mode security package to call back to its user-mode package and invoke a function in its DLL there.
old-location: security\clientcallback.htm
old-project: SecAuthN
ms.assetid: d818a7b5-15c8-4d25-a8de-050926f34a9d
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: ClientCallback, ClientCallback function [Security], LSA_CLIENT_CALLBACK, _ssp_clientcallback, ntsecpkg/ClientCallback, security.clientcallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: ntsecpkg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRUSTED_POSIX_OFFSET_INFO, *PTRUSTED_POSIX_OFFSET_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	Ntsecpkg.h
api_name:
-	ClientCallback
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_CLIENT_CALLBACK callback function


## -description


The <b>ClientCallback</b> function allows a <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA)-mode <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a> to call back to its user-mode package and invoke a function in its DLL there.


## -parameters




### -param Callback [in]

A pointer to the name of the function to invoke. For more information, see <a href="https://msdn.microsoft.com/52b4aa79-77ac-4065-a201-cc21a8d2277c">ClientCallback_Function</a>.


### -param Argument1 [in]

A pointer to the first argument to pass to the callback function.


### -param Argument2 [in]

A pointer to the second argument to pass to the callback function.


### -param Input [in]

A pointer to a 
<a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that contains information to pass to the callback function.


### -param Output [out]

A pointer to a <a href="https://msdn.microsoft.com/75f49d9c-7d3c-4f45-a94e-44cd05773a07">SecBuffer</a> structure that receives information passed from the callback function.


## -returns



If the function succeeds, the function returns STATUS_SUCCESS.

If the function fails, it returns an <b>NTSTATUS</b> code that indicates the reason it failed.




## -remarks



A pointer to the <b>ClientCallback</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.

The user-mode security package must use the 
<a href="https://msdn.microsoft.com/556f1fea-9675-4e2e-9fae-326e200cb98c">RegisterCallback</a> function to register the function to be called.




## -see-also




<a href="https://msdn.microsoft.com/52b4aa79-77ac-4065-a201-cc21a8d2277c">ClientCallback_Function</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/556f1fea-9675-4e2e-9fae-326e200cb98c">RegisterCallback</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

