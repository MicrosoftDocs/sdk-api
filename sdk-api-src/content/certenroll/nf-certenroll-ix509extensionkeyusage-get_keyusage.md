---
UID: NF:certenroll.IX509ExtensionKeyUsage.get_KeyUsage
title: IX509ExtensionKeyUsage::get_KeyUsage (certenroll.h)
author: windows-sdk-content
description: Retrieves the restrictions placed on the public key.
old-location: security\ix509extensionkeyusage_keyusage_property.htm
tech.root: seccertenroll
ms.assetid: ddb23d36-342f-4bd1-9936-72b025c4a03b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509ExtensionKeyUsage interface [Security],KeyUsage property, IX509ExtensionKeyUsage.KeyUsage, IX509ExtensionKeyUsage.get_KeyUsage, IX509ExtensionKeyUsage::KeyUsage, IX509ExtensionKeyUsage::get_KeyUsage, KeyUsage property [Security], KeyUsage property [Security],IX509ExtensionKeyUsage interface, certenroll/IX509ExtensionKeyUsage::KeyUsage, certenroll/IX509ExtensionKeyUsage::get_KeyUsage, get_KeyUsage, security.ix509extensionkeyusage_keyusage_property
ms.topic: method
f1_keywords: 
 - "certenroll/IX509ExtensionKeyUsage.KeyUsage"
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
 - IX509ExtensionKeyUsage.KeyUsage
 - IX509ExtensionKeyUsage.get_KeyUsage
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IX509ExtensionKeyUsage::get_KeyUsage


## -description


The <b>KeyUsage</b> property retrieves the restrictions placed on the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/p-gly">public key</a>.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionkeyusage-initializeencode">InitializeEncode</a> method or the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extensionkeyusage-initializedecode">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property to retrieve the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-ix509extensionkeyusage">IX509ExtensionKeyUsage</a>
 

 

