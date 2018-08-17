---
UID: NF:certenroll.IX509ExtensionEnhancedKeyUsage.get_EnhancedKeyUsage
title: IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage
author: windows-sdk-content
description: Retrieves a collection of key usage object identifiers (OIDs).
old-location: security\ix509extensionenhancedkeyusage_enhancedkeyusage_property.htm
old-project: seccertenroll
ms.assetid: 17a92139-0f6c-4371-b6cb-44185752abce
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: EnhancedKeyUsage property [Security], EnhancedKeyUsage property [Security],IX509ExtensionEnhancedKeyUsage interface, IX509ExtensionEnhancedKeyUsage interface [Security],EnhancedKeyUsage property, IX509ExtensionEnhancedKeyUsage.EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage.get_EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage::EnhancedKeyUsage, IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage, certenroll/IX509ExtensionEnhancedKeyUsage::EnhancedKeyUsage, certenroll/IX509ExtensionEnhancedKeyUsage::get_EnhancedKeyUsage, get_EnhancedKeyUsage, security.ix509extensionenhancedkeyusage_enhancedkeyusage_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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


The <b>EnhancedKeyUsage</b> property retrieves a collection of key usage <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifiers</a> (OIDs).

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378138(v=VS.85).aspx">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378135(v=VS.85).aspx">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the OID associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378132(v=VS.85).aspx">IX509ExtensionEnhancedKeyUsage</a>
 

 

