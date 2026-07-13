---
UID: NF:sspi.SaslIdentifyPackageA
title: SaslIdentifyPackageA function (sspi.h)
description: Returns the negotiate prefix that matches the specified SASL negotiation buffer. (ANSI)
helpviewer_keywords: ["SaslIdentifyPackageA", "sspi/SaslIdentifyPackageA"]
old-location: security\saslidentifypackage.htm
tech.root: security
ms.assetid: df6f4749-8f28-4ee5-8165-f7aeb3bea7ab
ms.date: 12/05/2018
ms.keywords: SaslIdentifyPackage, SaslIdentifyPackage function [Security], SaslIdentifyPackageA, SaslIdentifyPackageW, security.saslidentifypackage, sspi/SaslIdentifyPackage, sspi/SaslIdentifyPackageA, sspi/SaslIdentifyPackageW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaslIdentifyPackageA
 - sspi/SaslIdentifyPackageA
dev_langs:
 - c++
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
---

# SaslIdentifyPackageA function


## -description

The <b>SaslIdentifyPackage</b> function returns the  negotiate prefix that matches the specified SASL negotiation buffer.

## -parameters

### -param pInput [in]

Pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secbufferdesc">SecBufferDesc</a> structure that specifies the SASL negotiation buffer for which to find the negotiate prefix.

### -param PackageInfo [out]

Pointer to a pointer to a <a href="/windows/desktop/api/sspi/ns-sspi-secpkginfoa">SecPkgInfo</a> structure that returns the negotiate prefix for the negotiation buffer specified by the <i>pInput</i> parameter.

## -returns

If the call is completed successfully, this function returns SEC_E_OK.

If the function fails, the return value is a nonzero error code.

## -remarks

> [!NOTE]
> The sspi.h header defines SaslIdentifyPackage as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
