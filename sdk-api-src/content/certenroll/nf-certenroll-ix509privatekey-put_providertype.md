---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IX509PrivateKey::put_ProviderType


## -description


The <b>ProviderType</b> property specifies or retrieves the type of cryptographic provider associated with the <a href="https://msdn.microsoft.com/2fe6cfd3-8a2e-4dbe-9fb8-332633daa97a">private key</a>. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



You can use this property to force the use of the default provider for a given provider type. For example, to use the <b>PROV_RSA_SCHANNEL</b> provider, set this property to the <b>XCN_PROV_RSA_SCHANNEL</b><a href="https://msdn.microsoft.com/636ccb3a-ea66-4993-ac62-29409ce63eba">X509ProviderType</a> enumeration value and do not specify a value for the <a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a> property.

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
Because  a previously specified <a href="https://msdn.microsoft.com/library/windows/hardware/dn915743">ProviderName</a> is not affected by setting the <b>ProviderType</b> property, setting a <b>ProviderType</b> that is inconsistent with the <b>ProviderName</b> property will result in undefined behavior, likely a failure when creating or opening a private key. We recommend that you set the <b>ProviderType</b> property only when attempting to force the use of the default provider for the specified type as discussed above.




## -see-also




<a href="https://msdn.microsoft.com/72612ea4-ed45-46ac-9dad-614a9a754d83">IX509PrivateKey</a>
 

 

