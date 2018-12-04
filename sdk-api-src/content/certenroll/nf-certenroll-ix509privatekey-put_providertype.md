---
UID: NF:certenroll.IX509PrivateKey.put_ProviderType
title: IX509PrivateKey::put_ProviderType
author: windows-sdk-content
description: Specifies or retrieves the type of cryptographic provider associated with the private key.
old-location: security\ix509privatekey_providertype.htm
tech.root: seccertenroll
ms.assetid: 5f4d2e29-8c02-4d9c-a3a6-15c222650c3e
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IX509PrivateKey interface [Security],ProviderType property, IX509PrivateKey.ProviderType, IX509PrivateKey.put_ProviderType, IX509PrivateKey::ProviderType, IX509PrivateKey::get_ProviderType, IX509PrivateKey::put_ProviderType, ProviderType property [Security], ProviderType property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::ProviderType, certenroll/IX509PrivateKey::get_ProviderType, certenroll/IX509PrivateKey::put_ProviderType, put_ProviderType, security.ix509privatekey_providertype
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
 - IX509PrivateKey.ProviderType
 - IX509PrivateKey.get_ProviderType
 - IX509PrivateKey.put_ProviderType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509PrivateKey::put_ProviderType


## -description


The <b>ProviderType</b> property specifies or retrieves the type of cryptographic provider associated with the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



You can use this property to force the use of the default provider for a given provider type. For example, to use the <b>PROV_RSA_SCHANNEL</b> provider, set this property to the <b>XCN_PROV_RSA_SCHANNEL</b><a href="https://msdn.microsoft.com/636ccb3a-ea66-4993-ac62-29409ce63eba">X509ProviderType</a> enumeration value and do not specify a value for the <a href="https://msdn.microsoft.com/42a348ae-9946-4d76-a035-14990d823449">ProviderName</a> property.

Setting this property automatically sets the following properties to be consistent with the specified <b>ProviderType</b> value:

<ul>
<li>
<a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a>
</li>
</ul>
These properties are set in the following manner:

<ul>
<li>If the <b>ProviderType</b> is set to <b>XCN_PROV_NONE</b>:<ul>
<li>The <a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a> property is set to <b>VARIANT_FALSE</b>.</li>
<li>The <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property is set to <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
<li>If the <b>ProviderType</b> is not set to <b>XCN_PROV_NONE</b>:<ul>
<li>The <a href="https://msdn.microsoft.com/53a93aea-4435-4e04-9bd1-6356446aaefc">LegacyCsp</a> property is set to <b>VARIANT_TRUE</b>.</li>
<li>The <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property is set to <b>XCN_AT_SIGNATURE</b> if the  current value is <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
</ul>
Because  a previously specified <a href="https://msdn.microsoft.com/42a348ae-9946-4d76-a035-14990d823449">ProviderName</a> is not affected by setting the <b>ProviderType</b> property, setting a <b>ProviderType</b> that is inconsistent with the <b>ProviderName</b> property will result in undefined behavior, likely a failure when creating or opening a private key. We recommend that you set the <b>ProviderType</b> property only when attempting to force the use of the default provider for the specified type as discussed above.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

