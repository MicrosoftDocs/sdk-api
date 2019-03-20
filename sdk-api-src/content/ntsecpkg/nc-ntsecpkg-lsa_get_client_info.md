---
UID: NC:ntsecpkg.LSA_GET_CLIENT_INFO
title: LSA_GET_CLIENT_INFO (ntsecpkg.h)
author: windows-sdk-content
description: The GetClientInfo function gets information about the client process, such as thread and process ID, and flags indicating the client's state and privileges.
old-location: security\getclientinfo.htm
tech.root: SecAuthN
ms.assetid: 3669f2e2-da70-4195-bdd0-f8415d97ae99
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetClientInfo, GetClientInfo callback function [Security], LSA_GET_CLIENT_INFO, LSA_GET_CLIENT_INFO callback, _ssp_getclientinfo, ntsecpkg/GetClientInfo, security.getclientinfo
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
 - GetClientInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LSA_GET_CLIENT_INFO callback function


## -description


The <b>GetClientInfo</b> function gets information about the client process, such as thread and process ID, and flags indicating the client's state and privileges.


## -parameters




### -param ClientInfo [out]

Pointer to a 
<a href="https://msdn.microsoft.com/c9c58a50-7fc2-44a7-9551-a2675410b2b5">SECPKG_CLIENT_INFO</a> structure that receives information about the client.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code indicating the reason it failed.




## -remarks



A pointer to the <b>GetClientInfo</b> function is available in the 
<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a> structure received by the 
<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a> function.




## -see-also




<a href="https://msdn.microsoft.com/85f04072-8634-454a-9038-737d86c5597d">LSA_SECPKG_FUNCTION_TABLE</a>



<a href="https://msdn.microsoft.com/d93bafc6-d946-4214-b3c0-5e5a8e359638">SpInitialize</a>
 

 

