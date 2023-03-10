---
UID: NF:certenroll.IX509ExtensionSmimeCapabilities.get_SmimeCapabilities
title: IX509ExtensionSmimeCapabilities::get_SmimeCapabilities (certenroll.h)
description: Retrieves a collection of ISmimeCapability objects.
helpviewer_keywords: ["IX509ExtensionSmimeCapabilities interface [Security]","SmimeCapabilities property","IX509ExtensionSmimeCapabilities.SmimeCapabilities","IX509ExtensionSmimeCapabilities.get_SmimeCapabilities","IX509ExtensionSmimeCapabilities::SmimeCapabilities","IX509ExtensionSmimeCapabilities::get_SmimeCapabilities","SmimeCapabilities property [Security]","SmimeCapabilities property [Security]","IX509ExtensionSmimeCapabilities interface","certenroll/IX509ExtensionSmimeCapabilities::SmimeCapabilities","certenroll/IX509ExtensionSmimeCapabilities::get_SmimeCapabilities","get_SmimeCapabilities","security.ix509extensionsmimecapabilities_smimecapabilities"]
old-location: security\ix509extensionsmimecapabilities_smimecapabilities.htm
tech.root: security
ms.assetid: 6e3ce718-16f9-47df-aff9-38e922fe505c
ms.date: 12/05/2018
ms.keywords: IX509ExtensionSmimeCapabilities interface [Security],SmimeCapabilities property, IX509ExtensionSmimeCapabilities.SmimeCapabilities, IX509ExtensionSmimeCapabilities.get_SmimeCapabilities, IX509ExtensionSmimeCapabilities::SmimeCapabilities, IX509ExtensionSmimeCapabilities::get_SmimeCapabilities, SmimeCapabilities property [Security], SmimeCapabilities property [Security],IX509ExtensionSmimeCapabilities interface, certenroll/IX509ExtensionSmimeCapabilities::SmimeCapabilities, certenroll/IX509ExtensionSmimeCapabilities::get_SmimeCapabilities, get_SmimeCapabilities, security.ix509extensionsmimecapabilities_smimecapabilities
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
 - IX509ExtensionSmimeCapabilities::get_SmimeCapabilities
 - certenroll/IX509ExtensionSmimeCapabilities::get_SmimeCapabilities
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
 - IX509ExtensionSmimeCapabilities.SmimeCapabilities
 - IX509ExtensionSmimeCapabilities.get_SmimeCapabilities
---

# IX509ExtensionSmimeCapabilities::get_SmimeCapabilities


## -description

The <b>SmimeCapabilities</b> property retrieves a collection of <a href="/windows/desktop/api/certenroll/nn-certenroll-ismimecapability">ISmimeCapability</a> objects.

This property is read-only.

## -parameters

## -remarks

Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionsmimecapabilities-initializeencode">InitializeEncode</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensionsmimecapabilities-initializedecode">InitializeDecode</a> method to initialize the <b>SMIMECapabilities</b> extension.  You can also call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the OID associated with the extension.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensionsmimecapabilities">IX509ExtensionSmimeCapabilities</a>