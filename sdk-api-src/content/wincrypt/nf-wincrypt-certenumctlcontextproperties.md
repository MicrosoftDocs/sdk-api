---
UID: NF:wincrypt.CertEnumCTLContextProperties
title: CertEnumCTLContextProperties function (wincrypt.h)
description: The CertEnumCTLContextProperties function retrieves the first or next extended property associated with a certificate trust list (CTL) context. Used in a loop, this function can retrieve in sequence all extended properties associated with a CTL context.
helpviewer_keywords: ["CertEnumCTLContextProperties","CertEnumCTLContextProperties function [Security]","_crypto2_certenumctlcontextproperties","security.certenumctlcontextproperties","wincrypt/CertEnumCTLContextProperties"]
old-location: security\certenumctlcontextproperties.htm
tech.root: security
ms.assetid: f5c9c4cd-bf99-41bf-b13e-f1921b011039
ms.date: 12/05/2018
ms.keywords: CertEnumCTLContextProperties, CertEnumCTLContextProperties function [Security], _crypto2_certenumctlcontextproperties, security.certenumctlcontextproperties, wincrypt/CertEnumCTLContextProperties
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertEnumCTLContextProperties
 - wincrypt/CertEnumCTLContextProperties
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertEnumCTLContextProperties
---

# CertEnumCTLContextProperties function


## -description

The <b>CertEnumCTLContextProperties</b> function retrieves the first or next extended property associated with a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context. Used in a loop, this function can retrieve in sequence all extended properties associated with a CTL context.

## -parameters

### -param pCtlContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure.

### -param dwPropId [in]

Property number of the last property enumerated. To get the first property, <i>dwPropId</i> is zero. To retrieve subsequent properties, <i>dwPropId</i> is set to the property number returned by the last call to the function. To enumerate all the properties, function calls continue until the function returns zero. 




Applications can call 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetctlcontextproperty">CertGetCTLContextProperty</a> with the <i>dwPropId</i> returned by this function to retrieved that property's data.

## -returns

The return value is a <b>DWORD</b> value that identifies a CTL context's property. The <b>DWORD</b> value returned by one call of the function can be supplied as the <i>dwPropId</i> in a subsequent call to the function. If there are no more properties to be enumerated or if the function fails, zero is returned.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetctlcontextproperty">CertGetCTLContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Extended Property Functions</a>