---
UID: NF:sspi.QuerySecurityContextToken
title: QuerySecurityContextToken function (sspi.h)
author: windows-sdk-content
description: Obtains the access token for a client security context and uses it directly.
old-location: security\querysecuritycontexttoken.htm
tech.root: SecAuthN
ms.assetid: 5dc23608-9ce3-4fee-8161-2e409cef4063
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: QuerySecurityContextToken, QuerySecurityContextToken function [Security], _ssp_querysecuritycontexttoken, security.querysecuritycontexttoken, sspi/QuerySecurityContextToken
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
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
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - QuerySecurityContextToken
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# QuerySecurityContextToken function


## -description


Obtains the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">access token</a> for a client <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> and uses it directly.


## -parameters




### -param phContext [in]

Handle of the context to query.


### -param Token [out]

Returned handle to the access token.


## -returns



If the function succeeds, the function returns SEC_E_OK.

If the function fails, it returns a nonzero error code. One possible error code return is SEC_E_INVALID_HANDLE.




## -remarks



This function is called by a server application to control impersonation outside the SSPI layer, such as when launching a child process. The handle returned must be closed with <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> when the handle is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>
 

 

