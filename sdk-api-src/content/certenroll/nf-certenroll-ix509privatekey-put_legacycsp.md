---
UID: NF:certenroll.IX509PrivateKey.put_LegacyCsp
title: IX509PrivateKey::put_LegacyCsp
author: windows-sdk-content
description: Specifies or retrieves a Boolean value that indicates whether the provider is a CryptoAPI (legacy) cryptographic service provider (CSP).
old-location: security\ix509privatekey_legacycsp.htm
tech.root: seccertenroll
ms.assetid: 53a93aea-4435-4e04-9bd1-6356446aaefc
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IX509PrivateKey interface [Security],LegacyCsp property, IX509PrivateKey.LegacyCsp, IX509PrivateKey.put_LegacyCsp, IX509PrivateKey::LegacyCsp, IX509PrivateKey::get_LegacyCsp, IX509PrivateKey::put_LegacyCsp, LegacyCsp property [Security], LegacyCsp property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::LegacyCsp, certenroll/IX509PrivateKey::get_LegacyCsp, certenroll/IX509PrivateKey::put_LegacyCsp, put_LegacyCsp, security.ix509privatekey_legacycsp
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
 - IX509PrivateKey.LegacyCsp
 - IX509PrivateKey.get_LegacyCsp
 - IX509PrivateKey.put_LegacyCsp
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PrivateKey::put_LegacyCsp


## -description


The <b>LegacyCsp</b> property specifies  or retrieves a Boolean value that indicates whether the provider is a CryptoAPI (legacy) <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">cryptographic service provider</a> (CSP). This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



Setting this property automatically sets the following properties to be consistent with the specified <b>LegacyCsp</b> value:

<ul>
<li>
<a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a>
</li>
</ul>
These properties are set in the following manner:

<ul>
<li>If the <b>LegacyCsp</b> property is set to <b>VARIANT_FALSE</b>:<ul>
<li>The <a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a> is set to <b>XCN_PROV_NONE</b>.</li>
<li>The <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property is set to <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
<li>If the <b>LegacyCsp</b> property is set to <b>VARIANT_TRUE</b>:<ul>
<li>The <a href="https://msdn.microsoft.com/5f4d2e29-8c02-4d9c-a3a6-15c222650c3e">ProviderType</a> is set to <b>XCN_PROV_RSA_FULL</b> if the current value is <b>XCN_PROV_NONE</b>.</li>
<li>The <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property is set to <b>XCN_AT_SIGNATURE</b> if the current property is <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
</ul>
Because  a previously specified <a href="https://msdn.microsoft.com/42a348ae-9946-4d76-a035-14990d823449">ProviderName</a> is not affected by setting the <b>LegacyCsp</b> property, setting a <b>LegacyCsp</b> that is inconsistent with the <b>ProviderName</b> property will result in undefined behavior, likely a failure when creating or opening a private key.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

