---
UID: NF:certenroll.IX509ExtensionKeyUsage.get_KeyUsage
title: IX509ExtensionKeyUsage::get_KeyUsage
author: windows-sdk-content
description: Retrieves the restrictions placed on the public key.
old-location: security\ix509extensionkeyusage_keyusage_property.htm
old-project: seccertenroll
ms.assetid: ddb23d36-342f-4bd1-9936-72b025c4a03b
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IX509ExtensionKeyUsage interface [Security],KeyUsage property, IX509ExtensionKeyUsage.KeyUsage, IX509ExtensionKeyUsage.get_KeyUsage, IX509ExtensionKeyUsage::KeyUsage, IX509ExtensionKeyUsage::get_KeyUsage, KeyUsage property [Security], KeyUsage property [Security],IX509ExtensionKeyUsage interface, certenroll/IX509ExtensionKeyUsage::KeyUsage, certenroll/IX509ExtensionKeyUsage::get_KeyUsage, get_KeyUsage, security.ix509extensionkeyusage_keyusage_property
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
 - IX509ExtensionKeyUsage.KeyUsage
 - IX509ExtensionKeyUsage.get_KeyUsage
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionKeyUsage::get_KeyUsage


## -description


The <b>KeyUsage</b> property retrieves the restrictions placed on the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">public key</a>.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/a4496125-862c-4ef0-93f3-a513eedeacd1">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/5e51a148-0a76-4f38-b92f-fd5209e0b497">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="https://msdn.microsoft.com/library/windows/hardware/mt158256">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/4325e6aa-99bb-4c9a-9b19-c5352ebf27b9">IX509ExtensionKeyUsage</a>
 

 

