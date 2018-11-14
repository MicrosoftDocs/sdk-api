---
UID: NF:certenroll.IX509ExtensionKeyUsage.get_KeyUsage
title: IX509ExtensionKeyUsage::get_KeyUsage
author: windows-sdk-content
description: Retrieves the restrictions placed on the public key.
old-location: security\ix509extensionkeyusage_keyusage_property.htm
tech.root: SecCertEnroll
ms.assetid: ddb23d36-342f-4bd1-9936-72b025c4a03b
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509ExtensionKeyUsage interface [Security],KeyUsage property, IX509ExtensionKeyUsage.KeyUsage, IX509ExtensionKeyUsage.get_KeyUsage, IX509ExtensionKeyUsage::KeyUsage, IX509ExtensionKeyUsage::get_KeyUsage, KeyUsage property [Security], KeyUsage property [Security],IX509ExtensionKeyUsage interface, certenroll/IX509ExtensionKeyUsage::KeyUsage, certenroll/IX509ExtensionKeyUsage::get_KeyUsage, get_KeyUsage, security.ix509extensionkeyusage_keyusage_property
ms.prod: windows-hardware
ms.technology: windows-devices
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509ExtensionKeyUsage.get_KeyUsage
: 
---

# IX509ExtensionKeyUsage::get_KeyUsage


## -description


The <b>KeyUsage</b> property retrieves the restrictions placed on the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">public key</a>.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa378148(v=VS.85).aspx">InitializeEncode</a> method or the <a href="https://msdn.microsoft.com/en-us/library/Aa378146(v=VS.85).aspx">InitializeDecode</a> method to initialize the collection.  You can also call the <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property to specify and retrieve a Boolean value that identifies whether the extension is critical, and you can call the <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property to retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID) associated with the extension.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378144(v=VS.85).aspx">IX509ExtensionKeyUsage</a>
 

 

