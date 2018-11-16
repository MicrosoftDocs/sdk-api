---
UID: NF:certenroll.IX509AttributeCspProvider.get_KeySpec
title: IX509AttributeCspProvider::get_KeySpec
author: windows-sdk-content
description: Retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.
old-location: security\ix509attributecspprovider_keyspec_property.htm
tech.root: SecCertEnroll
ms.assetid: 4bb04097-9e6c-4b15-852e-be86d21637bf
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509AttributeCspProvider interface [Security],KeySpec property, IX509AttributeCspProvider.KeySpec, IX509AttributeCspProvider.get_KeySpec, IX509AttributeCspProvider::KeySpec, IX509AttributeCspProvider::get_KeySpec, KeySpec property [Security], KeySpec property [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::KeySpec, certenroll/IX509AttributeCspProvider::get_KeySpec, get_KeySpec, security.ix509attributecspprovider_keyspec_property
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
 - IX509AttributeCspProvider.KeySpec
 - IX509AttributeCspProvider.get_KeySpec
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
- IX509AttributeCspProvider.get_KeySpec
: 
---

# IX509AttributeCspProvider::get_KeySpec


## -description


The <b>KeySpec</b> property retrieves a value that identifies whether the key pair stored by the provider or key container is used for encryption or for signing content.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377084(v=VS.85).aspx">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/en-us/library/Aa377083(v=VS.85).aspx">InitializeDecode</a> method to initialize the <b>KeySpec</b> property. You can also call the following properties to retrieve raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377088(v=VS.85).aspx">ProviderName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377089(v=VS.85).aspx">Signature</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377082(v=VS.85).aspx">IX509AttributeCspProvider</a>
 

 

