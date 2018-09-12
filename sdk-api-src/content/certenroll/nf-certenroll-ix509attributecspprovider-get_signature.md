---
UID: NF:certenroll.IX509AttributeCspProvider.get_Signature
title: IX509AttributeCspProvider::get_Signature
author: windows-sdk-content
description: Retrieves the digital signature on the provider.
old-location: security\ix509attributecspprovider_signature_property.htm
tech.root: SecCertEnroll
ms.assetid: 06245293-b331-4963-a0cf-b7c604580908
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509AttributeCspProvider interface [Security],Signature property, IX509AttributeCspProvider.Signature, IX509AttributeCspProvider.get_Signature, IX509AttributeCspProvider::Signature, IX509AttributeCspProvider::get_Signature, Signature property [Security], Signature property [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::Signature, certenroll/IX509AttributeCspProvider::get_Signature, get_Signature, security.ix509attributecspprovider_signature_property
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
 - IX509AttributeCspProvider.Signature
 - IX509AttributeCspProvider.get_Signature
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeCspProvider::get_Signature


## -description


The <b>Signature</b> property retrieves the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">digital signature</a> on the provider. The signature is contained in a byte array represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/b0b45ea2-b682-4065-8624-08c34581b5ea">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/7098ee8d-39e9-4463-97fe-309265c6baa7">InitializeDecode</a> method to initialize the <b>Signature</b> property. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/4bb04097-9e6c-4b15-852e-be86d21637bf">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4a62d1e4-4d00-416b-b44a-23a9cbc53a5b">ProviderName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a>
 

 

