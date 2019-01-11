---
UID: NC:ntsecpkg.LSA_OPEN_TOKEN_BY_LOGON_ID
title: LSA_OPEN_TOKEN_BY_LOGON_ID
author: windows-sdk-content
description: Opens the user access token associated with the specified user logon.
old-location: security\opentokenbylogonid.htm
tech.root: SecAuthN
ms.assetid: 3cd3e4fe-7548-44f9-ab04-01b30bdf3bd9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: LSA_OPEN_TOKEN_BY_LOGON_ID, LSA_OPEN_TOKEN_BY_LOGON_ID callback, OpenTokenByLogonId, OpenTokenByLogonId callback function [Security], ntsecpkg/OpenTokenByLogonId, security.opentokenbylogonid
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Ntsecpkg.h
api_name:
 - OpenTokenByLogonId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LSA_OPEN_TOKEN_BY_LOGON_ID callback function


## -description


Opens the user access token associated with the specified user logon.


## -parameters




### -param LogonId [in]

A pointer to a <a href="https://msdn.microsoft.com/a812a46b-f23f-45b1-a6c6-48f931b78750">LUID</a> structure that identifies the user for which to open the access token.


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
 

 

