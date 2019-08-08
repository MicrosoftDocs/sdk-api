---
UID: NF:sspi.QuerySecurityPackageInfoW
title: QuerySecurityPackageInfoW function (sspi.h)
author: windows-sdk-content
description: Retrieves information about a specified security package. This information includes the bounds on sizes of authentication information, credentials, and contexts.
old-location: security\querysecuritypackageinfo.htm
tech.root: SecAuthN
ms.assetid: 130ef0fe-bb13-4a65-b476-cd25ed234da1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: QuerySecurityPackageInfo, QuerySecurityPackageInfo function [Security], QuerySecurityPackageInfoA, QuerySecurityPackageInfoW, _ssp_querysecuritypackageinfo, security.querysecuritypackageinfo, sspi/QuerySecurityPackageInfo, sspi/QuerySecurityPackageInfoA, sspi/QuerySecurityPackageInfoW
ms.topic: function
f1_keywords:
- sspi/QuerySecurityPackageInfo
req.header: sspi.h
req.include-header: Security.h
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
- QuerySecurityPackageInfo
- QuerySecurityPackageInfoA
- QuerySecurityPackageInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# QuerySecurityPackageInfoW function


## -description


Retrieves information about a specified <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security package</a>. This information includes the bounds on sizes of authentication information, <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">credentials</a>, and contexts.


## -parameters




### -param pPackageName

TBD


### -param ppPackageInfo [out]

Pointer to a variable that receives a pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure containing information about the specified security package.


#### - pszPackageName [in]

Pointer to a null-terminated string that specifies the name of the security package.


## -returns



If the function succeeds, the return value is SEC_E_OK.

If the function fails, the return value is a nonzero error code.




## -remarks



The caller must call the 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a> function to free the buffer returned in <i>ppPackageInfo</i>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-freecontextbuffer">FreeContextBuffer</a>



<a href="https://docs.microsoft.com/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a>
 

 

