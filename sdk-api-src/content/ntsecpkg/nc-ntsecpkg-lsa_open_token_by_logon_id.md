---
UID: NC:ntsecpkg.LSA_OPEN_TOKEN_BY_LOGON_ID
title: LSA_OPEN_TOKEN_BY_LOGON_ID
author: windows-driver-content
description: Opens the user access token associated with the specified user logon.
old-location: security\opentokenbylogonid.htm
old-project: SecAuthN
ms.assetid: 3cd3e4fe-7548-44f9-ab04-01b30bdf3bd9
ms.author: windowsdriverdev
ms.date: 3/29/2018
ms.keywords: LSA_OPEN_TOKEN_BY_LOGON_ID, OpenTokenByLogonId, OpenTokenByLogonId function [Security], ntsecpkg/OpenTokenByLogonId, security.opentokenbylogonid
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
-	OpenTokenByLogonId
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# LSA_OPEN_TOKEN_BY_LOGON_ID callback


## -description


Opens the user access token associated with the specified user logon.


## -parameters




### -param LogonId [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff557080">LUID</a> structure that identifies the user for which to open the access token.


### -param *RetTokenHandle [out]

A pointer to the handle to the token this function opens.


## -returns



If the function succeeds, return STATUS_SUCCESS, or an informational status code.

If the function fails, return an NTSTATUS error code that indicates the reason it failed.




## -remarks



A pointer to the <b>OpenTokenByLogonId</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

