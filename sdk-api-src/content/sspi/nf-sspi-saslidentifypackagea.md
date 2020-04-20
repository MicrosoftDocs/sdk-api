---
UID: NF:sspi.SaslIdentifyPackageA
title: SaslIdentifyPackageA function (sspi.h)
description: Returns the negotiate prefix that matches the specified SASL negotiation buffer.helpviewer_keywords: ["SaslIdentifyPackage","SaslIdentifyPackage function [Security]","SaslIdentifyPackageA","SaslIdentifyPackageW","security.saslidentifypackage","sspi/SaslIdentifyPackage","sspi/SaslIdentifyPackageA","sspi/SaslIdentifyPackageW"]
old-location: security\saslidentifypackage.htm
tech.root: SecAuthN
ms.assetid: df6f4749-8f28-4ee5-8165-f7aeb3bea7ab
ms.date: 12/05/2018
ms.keywords: SaslIdentifyPackage, SaslIdentifyPackage function [Security], SaslIdentifyPackageA, SaslIdentifyPackageW, security.saslidentifypackage, sspi/SaslIdentifyPackage, sspi/SaslIdentifyPackageA, sspi/SaslIdentifyPackageW
f1_keywords:
- sspi/SaslIdentifyPackage
dev_langs:
- c++
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SaslIdentifyPackageW (Unicode) and SaslIdentifyPackageA (ANSI)
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
- SaslIdentifyPackage
- SaslIdentifyPackageA
- SaslIdentifyPackageW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# SaslIdentifyPackageA function


## -description


The <b>SaslIdentifyPackage</b> function returns the  negotiate prefix that matches the specified SASL negotiation buffer.  


## -parameters




### -param pInput [in]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that specifies the SASL negotiation buffer for which to find the negotiate prefix. 


### -param PackageInfo [out]

Pointer to a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure that returns the negotiate prefix for the negotiation buffer specified by the <i>pInput</i> parameter.


## -returns



If the call is completed successfully, this function returns SEC_E_OK.

If the function fails, the return value is a nonzero error code.



