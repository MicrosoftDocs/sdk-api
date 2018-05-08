---
UID: NC:ntsecpkg.LSA_GET_USER_AUTH_DATA
title: LSA_GET_USER_AUTH_DATA
author: windows-driver-content
description: The GetUserAuthData function returns the authorization data for the user in a single buffer.
old-location: security\getuserauthdata.htm
old-project: SecAuthN
ms.assetid: 2436eaee-1f32-4e32-9a98-74968ad9b58e
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: GetUserAuthData, GetUserAuthData function [Security], LSA_GET_USER_AUTH_DATA, _ssp_getuserauthdata, ntsecpkg/GetUserAuthData, security.getuserauthdata
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
-	GetUserAuthData
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LSA_GET_USER_AUTH_DATA callback function


## -description


The <b>GetUserAuthData</b> function returns the authorization data for the user in a single buffer.


## -parameters




### -param UserHandle [in]

A handle to the user account. This handle is returned by the 
<a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a> function.


### -param *UserAuthData [out]

Pointer that receives the consolidated authorization data. When you have finished using the authorization data, free the memory by calling the <a href="https://msdn.microsoft.com/bd461a23-2501-48c5-8f2f-c6c98383157f">FreeLsaHeap</a> function.


### -param UserAuthDataSize [out]

Pointer that receives the size of the authorization data.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.




## -remarks



The authorization data returned by the <b>GetUserAuthData</b> function can be passed to the 
<a href="https://msdn.microsoft.com/99dfd3b3-40e0-44b2-8752-39b7b394ac0e">ConvertAuthDataToToken</a> function.

A pointer to the <b>GetUserAuthData</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/99dfd3b3-40e0-44b2-8752-39b7b394ac0e">ConvertAuthDataToToken</a>



<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/1d9bfbe5-8dd2-4b0f-a19a-361eef8901a4">OpenSamUser</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

