---
UID: NF:certenroll.IX509AttributeCspProvider.get_KeySpec
title: IX509AttributeCspProvider::get_KeySpec (certenroll.h)
author: windows-sdk-content
description: Retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.
old-location: security\ix509attributecspprovider_keyspec_property.htm
tech.root: seccertenroll
ms.assetid: 4bb04097-9e6c-4b15-852e-be86d21637bf
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509AttributeCspProvider interface [Security],KeySpec property, IX509AttributeCspProvider.KeySpec, IX509AttributeCspProvider.get_KeySpec, IX509AttributeCspProvider::KeySpec, IX509AttributeCspProvider::get_KeySpec, KeySpec property [Security], KeySpec property [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::KeySpec, certenroll/IX509AttributeCspProvider::get_KeySpec, get_KeySpec, security.ix509attributecspprovider_keyspec_property
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
 - IX509AttributeCspProvider.KeySpec
 - IX509AttributeCspProvider.get_KeySpec
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509AttributeCspProvider::get_KeySpec


## -description


The <b>KeySpec</b> property retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/b0b45ea2-b682-4065-8624-08c34581b5ea">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/7098ee8d-39e9-4463-97fe-309265c6baa7">InitializeDecode</a> method to initialize the <b>KeySpec</b> property. You can also call the following properties to retrieve raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/4a62d1e4-4d00-416b-b44a-23a9cbc53a5b">ProviderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06245293-b331-4963-a0cf-b7c604580908">Signature</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/08954c87-f63b-4e1a-91b4-3773e392999b">IX509AttributeCspProvider</a>
 

 

