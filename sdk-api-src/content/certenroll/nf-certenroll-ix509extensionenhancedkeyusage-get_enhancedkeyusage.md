---
UID: NF:certenroll.IX509ExtensionEnhancedKeyUsage.get_EnhancedKeyUsage
title: IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage
author: windows-sdk-content
description: Retrieves a collection of key usage object identifiers (OIDs).
old-location: security\ix509extensionenhancedkeyusage_enhancedkeyusage_property.htm
old-project: SecCertEnroll
ms.assetid: 17a92139-0f6c-4371-b6cb-44185752abce
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: EnhancedKeyUsage property [Security], EnhancedKeyUsage property [Security],IX509ExtensionEnhancedKeyUsage interface, IX509ExtensionEnhancedKeyUsage interface [Security],EnhancedKeyUsage property, IX509ExtensionEnhancedKeyUsage.EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage.get_EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage::EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage, certenroll/IX509ExtensionEnhancedKeyUsage::EnhancedKeyUsage, certenroll/IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage, get_EnhancedKeyUsage, security.ix509extensionenhancedkeyusage_enhancedkeyusage_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage


## -description


The <b>EnhancedKeyUsage</b> property retrieves a collection of key usage <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifiers</a> (OIDs).

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/6cb12736-db5d-4d65-b32f-4bd11ceea01d">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/e83d0577-8eb9-4a59-8f52-ce1d9ab7f58a">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property to retrieve the OID associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/0b9606d0-351c-4d2d-b876-545a9c2cf916">IX509ExtensionEnhancedKeyUsage</a>
 

 

