---
UID: NC:ntsecpkg.LSA_GET_CALL_INFO
title: LSA_GET_CALL_INFO
author: windows-driver-content
description: The GetCallInfo function retrieves information about the most recent function call.
old-location: security\getcallinfo.htm
old-project: SecAuthN
ms.assetid: 3e59ee6a-f7ba-4886-98f7-74ffbfaadea7
ms.author: windowsdriverdev
ms.date: 5/14/2018
ms.keywords: GetCallInfo, GetCallInfo function [Security], LSA_GET_CALL_INFO, _ssp_getcallinfo, ntsecpkg/GetCallInfo, security.getcallinfo
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
-	GetCallInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# LSA_GET_CALL_INFO callback function


## -description


The <b>GetCallInfo</b> function retrieves information about the most recent function call.


## -parameters




### -param Info [out]

Pointer to a 
<a href="https://msdn.microsoft.com/ac25ef88-7c64-42dd-8daa-fad039453043">SECPKG_CALL_INFO</a> structure that receives information about the call.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>.




## -remarks



A pointer to the <b>GetCallInfo</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

