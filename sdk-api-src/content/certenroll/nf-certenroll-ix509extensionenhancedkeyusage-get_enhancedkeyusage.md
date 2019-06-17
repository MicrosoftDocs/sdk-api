---
UID: NF:certenroll.IX509ExtensionEnhancedKeyUsage.get_EnhancedKeyUsage
title: IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage (certenroll.h)
author: windows-sdk-content
description: Retrieves a collection of key usage object identifiers (OIDs).
old-location: security\ix509extensionenhancedkeyusage_enhancedkeyusage_property.htm
tech.root: seccertenroll
ms.assetid: 17a92139-0f6c-4371-b6cb-44185752abce
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EnhancedKeyUsage property [Security], EnhancedKeyUsage property [Security],IX509ExtensionEnhancedKeyUsage interface, IX509ExtensionEnhancedKeyUsage interface [Security],EnhancedKeyUsage property, IX509ExtensionEnhancedKeyUsage.EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage.get_EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage::EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage, certenroll/IX509ExtensionEnhancedKeyUsage::EnhancedKeyUsage, certenroll/IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage, get_EnhancedKeyUsage, security.ix509extensionenhancedkeyusage_enhancedkeyusage_property
ms.topic: method
f1_keywords: ["certenroll/IX509ExtensionEnhancedKeyUsage.EnhancedKeyUsage"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509ExtensionEnhancedKeyUsage.EnhancedKeyUsage
 - IX509ExtensionEnhancedKeyUsage.get_EnhancedKeyUsage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage


## -description


The <b>EnhancedKeyUsage</b> property retrieves a collection of key usage <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs).

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionenhancedkeyusage-initializeencode">InitializeEncode</a> method or the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionenhancedkeyusage-initializedecode">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the OID associated with the extension.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionenhancedkeyusage">IX509ExtensionEnhancedKeyUsage</a>
 

 

