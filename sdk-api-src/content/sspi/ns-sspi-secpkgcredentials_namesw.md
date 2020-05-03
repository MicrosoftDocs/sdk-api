---
UID: NS:sspi._SecPkgCredentials_NamesW
title: SecPkgCredentials_NamesW (sspi.h)
description: The SecPkgCredentials_Names structure holds the name of the user associated with a context. The QueryCredentialsAttributes function uses this structure.helpviewer_keywords: ["*PSecPkgCredentials_NamesW","PSecPkgCredentials_Names","PSecPkgCredentials_Names structure pointer [Security]","SecPkgCredentials_Names","SecPkgCredentials_Names structure [Security]","SecPkgCredentials_NamesA","SecPkgCredentials_NamesW","_ssp_secpkgcredentials_names","security.secpkgcredentials_names","sspi/PSecPkgCredentials_Names","sspi/SecPkgCredentials_Names","sspi/SecPkgCredentials_NamesA","sspi/SecPkgCredentials_NamesW"]
old-location: security\secpkgcredentials_names.htm
tech.root: SecAuthN
ms.assetid: 38123a10-72a4-46eb-974b-3c01142dfc74
ms.date: 12/05/2018
ms.keywords: '*PSecPkgCredentials_NamesW, PSecPkgCredentials_Names, PSecPkgCredentials_Names structure pointer [Security], SecPkgCredentials_Names, SecPkgCredentials_Names structure [Security], SecPkgCredentials_NamesA, SecPkgCredentials_NamesW, _ssp_secpkgcredentials_names, security.secpkgcredentials_names, sspi/PSecPkgCredentials_Names, sspi/SecPkgCredentials_Names, sspi/SecPkgCredentials_NamesA, sspi/SecPkgCredentials_NamesW'
f1_keywords:
- sspi/SecPkgCredentials_Names
dev_langs:
- c++
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgCredentials_NamesW (Unicode) and SecPkgCredentials_NamesA (ANSI)
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
- HeaderDef
api_location:
- Sspi.h
api_name:
- SecPkgCredentials_Names
- SecPkgCredentials_NamesA
- SecPkgCredentials_NamesW
targetos: Windows
req.typenames: SecPkgCredentials_NamesW, *PSecPkgCredentials_NamesW
req.redist: 
ms.custom: 19H1
---

# SecPkgCredentials_NamesW structure


## -description


The <b>SecPkgCredentials_Names</b> structure holds the name of the user associated with a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">context</a>. The 
<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycredentialsattributesa">QueryCredentialsAttributes</a> function uses this structure.


## -struct-fields




### -field sUserName

Pointer to a null-terminated string containing the name of the user represented by the credential. If the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security package</a> sets the SECPKG_FLAG_ACCEPT_WIN32_NAME flag to indicate that it can process Windows names, this name can be used in other Windows calls.


### -field sUserName.string

 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/sspi/nf-sspi-querycredentialsattributesa">QueryCredentialsAttributes</a>
 

 

