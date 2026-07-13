---
UID: NF:sspi.InitSecurityInterfaceW
title: InitSecurityInterfaceW function (sspi.h)
description: The InitSecurityInterface function returns a pointer to an SSPI dispatch table. This function enables clients to use SSPI without binding directly to an implementation of the interface. (Unicode)
helpviewer_keywords: ["InitSecurityInterface", "InitSecurityInterface function [Security]", "InitSecurityInterfaceW", "_ssp_initsecurityinterface", "security.initsecurityinterface", "sspi/InitSecurityInterface", "sspi/InitSecurityInterfaceW"]
old-location: security\initsecurityinterface.htm
tech.root: security
ms.assetid: 1026eeab-e2d6-45f2-9677-82d6cfbf4e12
ms.date: 12/05/2018
ms.keywords: InitSecurityInterface, InitSecurityInterface function [Security], InitSecurityInterfaceA, InitSecurityInterfaceW, _ssp_initsecurityinterface, security.initsecurityinterface, sspi/InitSecurityInterface, sspi/InitSecurityInterfaceA, sspi/InitSecurityInterfaceW
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: InitSecurityInterfaceW (Unicode) and InitSecurityInterfaceA (ANSI)
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
 - InitSecurityInterfaceW
 - sspi/InitSecurityInterfaceW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
 - security.dll
 - schannel.dll
 - kernel32.dll
api_name:
 - InitSecurityInterface
 - InitSecurityInterfaceA
 - InitSecurityInterfaceW
---

# InitSecurityInterfaceW function


## -description

The <b>InitSecurityInterface</b> function returns a pointer to an SSPI dispatch table. This function enables clients to use SSPI without binding directly to an implementation of the interface.



## -returns

If the function succeeds, the return value is a pointer to a 
<a href="/windows/win32/api/sspi/ns-sspi-securityfunctiontablea">SecurityFunctionTable</a> structure.

If the function fails, the return value is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/SecAuthN/authentication-functions">SSPI Functions</a>



<a href="/windows/win32/api/sspi/ns-sspi-securityfunctiontablea">SecurityFunctionTable</a>

## -remarks

> [!NOTE]
> The sspi.h header defines InitSecurityInterface as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
