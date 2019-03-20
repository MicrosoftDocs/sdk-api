---
UID: NS:schannel._SecPkgContext_KeyingMaterialInfo
title: SecPkgContext_KeyingMaterialInfo (schannel.h)
author: windows-sdk-content
description: The SecPkgContext_KeyingMaterialInfo structure contains information about the exportable keying material in a security context.
old-location: security\secpkgcontext_keyingmaterialinfo.htm
tech.root: SecAuthN
ms.assetid: 51EE7027-01FA-4D2F-9FB8-EEF7C1479600
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PSecPkgContext_KeyingMaterialInfo, PSecPkgContext_KeyingMaterialInfo, PSecPkgContext_KeyingMaterialInfo structure pointer [Security], SecPkgContext_KeyingMaterialInfo, SecPkgContext_KeyingMaterialInfo structure [Security], SecPkgContext_KeyingMaterialInfoA, SecPkgContext_KeyingMaterialInfoW, _SecPkgContext_KeyingMaterialInfo, security.secpkgcontext_keyingmaterialinfo, sspi/PSecPkgContext_KeyingMaterialInfo, sspi/SecPkgContext_KeyingMaterialInfo, sspi/SecPkgContext_KeyingMaterialInfoA, sspi/SecPkgContext_KeyingMaterialInfoW"
ms.topic: struct
req.header: schannel.h
req.include-header: Schannel.h, Security.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SecPkgContext_KeyingMaterialInfoW (Unicode) and SecPkgContext_KeyingMaterialInfoA (ANSI)
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
 - SecPkgContext_KeyingMaterialInfo
 - SecPkgContext_KeyingMaterialInfoA
 - SecPkgContext_KeyingMaterialInfoW
product: Windows
targetos: Windows
req.typenames: SecPkgContext_KeyingMaterialInfo, *PSecPkgContext_KeyingMaterialInfo
req.redist: 
---

# SecPkgContext_KeyingMaterialInfo structure


## -description


The <b>SecPkgContext_KeyingMaterialInfo</b> structure contains information about the exportable keying material in a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a>. 


## -struct-fields




### -field cbLabel

The length, in bytes, of the disambiguating ASCII label, including NUL terminator.


### -field pszLabel

 A NUL-terminated ASCII string. The NUL terminator will be removed by schannel before mixing in pszLabel. 

IANA-registered labels should begin with "EXPORTER" to  avoid collisions with existing PRF labels. Labels beginning with "EXPERIMENTAL" may be used without registration.


### -field cbContextValue

 


### -field pbContextValue

The pointer to the application context. Must be <b>NULL</b> if <i>cbContextValue</i> is zero.


### -field cbKeyingMaterial

The length, in bytes, of the keying material to be generated. Must be greater than zero.


#### - cbConextValue

The length, in bytes, of the application context. Zero if application context is not provided by the caller.

