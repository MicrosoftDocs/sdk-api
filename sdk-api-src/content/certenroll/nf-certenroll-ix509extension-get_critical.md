---
UID: NF:certenroll.IX509Extension.get_Critical
title: IX509Extension::get_Critical (certenroll.h)
description: Specifies and retrieves a Boolean value that identifies whether the certificate extension is critical. (Get)
helpviewer_keywords: ["Critical property [Security]","Critical property [Security]","IX509Extension interface","IX509Extension interface [Security]","Critical property","IX509Extension.Critical","IX509Extension.get_Critical","IX509Extension::Critical","IX509Extension::get_Critical","IX509Extension::put_Critical","certenroll/IX509Extension::Critical","certenroll/IX509Extension::get_Critical","certenroll/IX509Extension::put_Critical","get_Critical","security.ix509extension_critical_property"]
old-location: security\ix509extension_critical_property.htm
tech.root: security
ms.assetid: b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072
ms.date: 12/05/2018
ms.keywords: Critical property [Security], Critical property [Security],IX509Extension interface, IX509Extension interface [Security],Critical property, IX509Extension.Critical, IX509Extension.get_Critical, IX509Extension::Critical, IX509Extension::get_Critical, IX509Extension::put_Critical, certenroll/IX509Extension::Critical, certenroll/IX509Extension::get_Critical, certenroll/IX509Extension::put_Critical, get_Critical, security.ix509extension_critical_property
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: CertEnroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509Extension::get_Critical
 - certenroll/IX509Extension::get_Critical
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509Extension.Critical
 - IX509Extension.get_Critical
 - IX509Extension.put_Critical
---

# IX509Extension::get_Critical


## -description

The <b>Critical</b> property specifies and retrieves a Boolean value that identifies whether the certificate extension is critical. This property is web enabled on input.

This property is read/write.

## -parameters

## -remarks

A certificate extension consists of an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID), a Boolean value that identifies whether the extension is critical, and a byte array that contains the extension value. The criticality indicates whether an application that uses a certificate can ignore the extension type and value. If an extension is identified as critical but the application does not recognize the extension type, the application should reject the certificate.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extension">IX509Extension</a>
