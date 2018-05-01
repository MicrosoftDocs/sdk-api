---
UID: NF:certenroll.IX509PrivateKey.put_ProviderName
title: IX509PrivateKey::put_ProviderName method
author: windows-driver-content
description: Specifies or retrieves the name of the cryptographic provider.
old-location: security\ix509privatekey_providername.htm
old-project: SecCertEnroll
ms.assetid: 42a348ae-9946-4d76-a035-14990d823449
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: IX509PrivateKey, IX509PrivateKey interface [Security], ProviderName property, IX509PrivateKey.ProviderName, IX509PrivateKey::get_ProviderName, IX509PrivateKey::put_ProviderName, ProviderName property [Security], ProviderName property [Security], IX509PrivateKey interface, certenroll/IX509PrivateKey::ProviderName, certenroll/IX509PrivateKey::get_ProviderName, certenroll/IX509PrivateKey::put_ProviderName, put_ProviderName,IX509PrivateKey.put_ProviderName, security.ix509privatekey_providername
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
-	IX509PrivateKey.ProviderName
-	IX509PrivateKey.get_ProviderName
-	IX509PrivateKey.put_ProviderName
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509PrivateKey::put_ProviderName method


## -description


The <b>ProviderName</b> property specifies or retrieves the name of the cryptographic provider. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



Setting this property automatically sets the following properties to be consistent with the specified <b>ProviderName</b> value:

<ul>
<li>
<a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a>
</li>
</ul>
These properties are set in the following manner:

<ul>
<li>The provider configuration data is used, if available, to determine the appropriate <a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a> value.</li>
<li>If the specified provider is a CNG KSP:<ul>
<li>The <a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a> property is set to <b>VARIANT_FALSE</b>.</li>
<li>The <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property is set to <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
<li>If the specified provider is not a CNG KSP:<ul>
<li>The <a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a> property is set to <b>VARIANT_TRUE</b>.</li>
<li>The <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property is set to <b>XCN_AT_SIGNATURE</b>.</li>
</ul>
</li>
</ul>
If you set the <b>ProviderName</b> property, we recommend that you do not set the <a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a> or <a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a> properties.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

