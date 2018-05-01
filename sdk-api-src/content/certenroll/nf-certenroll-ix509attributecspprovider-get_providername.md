---
UID: NF:certenroll.IX509AttributeCspProvider.get_ProviderName
title: IX509AttributeCspProvider::get_ProviderName method
author: windows-driver-content
description: Retrieves the provider name.
old-location: security\ix509attributecspprovider_providername_property.htm
old-project: SecCertEnroll
ms.assetid: 4a62d1e4-4d00-416b-b44a-23a9cbc53a5b
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509AttributeCspProvider, IX509AttributeCspProvider interface [Security], ProviderName property, IX509AttributeCspProvider.ProviderName, IX509AttributeCspProvider::get_ProviderName, ProviderName property [Security], ProviderName property [Security], IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::ProviderName, certenroll/IX509AttributeCspProvider::get_ProviderName, get_ProviderName,IX509AttributeCspProvider.get_ProviderName, security.ix509attributecspprovider_providername_property
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
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509AttributeCspProvider.ProviderName
-	IX509AttributeCspProvider.get_ProviderName
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeCspProvider::get_ProviderName method


## -description


The <b>ProviderName</b> property retrieves the provider name.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/b0b45ea2-b682-4065-8624-08c34581b5ea">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/7098ee8d-39e9-4463-97fe-309265c6baa7">InitializeDecode</a> method to initialize the <b>ProviderName</b> property. You can also call the following properties to retrieve raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/4bb04097-9e6c-4b15-852e-be86d21637bf">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06245293-b331-4963-a0cf-b7c604580908">Signature</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a>
 

 

