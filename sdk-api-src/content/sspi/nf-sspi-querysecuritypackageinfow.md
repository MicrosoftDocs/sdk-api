---
UID: NF:sspi.QuerySecurityPackageInfoW
title: QuerySecurityPackageInfoW function
author: windows-sdk-content
description: Retrieves information about a specified security package. This information includes the bounds on sizes of authentication information, credentials, and contexts.
old-location: security\querysecuritypackageinfo.htm
old-project: secauthn
ms.assetid: 130ef0fe-bb13-4a65-b476-cd25ed234da1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: QuerySecurityPackageInfo, QuerySecurityPackageInfo function [Security], QuerySecurityPackageInfoA, QuerySecurityPackageInfoW, _ssp_querysecuritypackageinfo, security.querysecuritypackageinfo, sspi/QuerySecurityPackageInfo, sspi/QuerySecurityPackageInfoA, sspi/QuerySecurityPackageInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: QuerySecurityPackageInfoW (Unicode) and QuerySecurityPackageInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS, *PSEC_APPLICATION_PROTOCOL_NEGOTIATION_STATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - QuerySecurityPackageInfo
 - QuerySecurityPackageInfoA
 - QuerySecurityPackageInfoW
product: Windows
targetos: Windows
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
req.product: Outlook Express 6.0
---

# QuerySecurityPackageInfoW function


## -description


Retrieves information about a specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>. This information includes the bounds on sizes of authentication information, <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">credentials</a>, and contexts.


## -parameters




#### - pPackageName [in]

Pointer to a null-terminated string that specifies the name of the security package.


### -param ppPackageInfo [out]

Pointer to a variable that receives a pointer to a 
<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a> structure containing information about the specified security package.


## -returns



If the function succeeds, the return value is SEC_E_OK.

If the function fails, the return value is a nonzero error code.




## -remarks



The caller must call the 
<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a> function to free the buffer returned in <i>ppPackageInfo</i>.




## -see-also




<a href="https://msdn.microsoft.com/3c3d27bb-4f9a-4979-b679-1e10fa1ff221">FreeContextBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa374731(v=VS.85).aspx">SSPI Functions</a>



<a href="https://msdn.microsoft.com/d0bff3d8-63f1-4a4e-851f-177040af6bd2">SecPkgInfo</a>
 

 

