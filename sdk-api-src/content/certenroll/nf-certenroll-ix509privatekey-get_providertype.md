---
UID: NF:certenroll.IX509PrivateKey.get_ProviderType
title: IX509PrivateKey::get_ProviderType
author: windows-sdk-content
description: Specifies or retrieves the type of cryptographic provider associated with the private key.
old-location: security\ix509privatekey_providertype.htm
tech.root: SecCertEnroll
ms.assetid: 5f4d2e29-8c02-4d9c-a3a6-15c222650c3e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IX509PrivateKey interface [Security],ProviderType property, IX509PrivateKey.ProviderType, IX509PrivateKey.get_ProviderType, IX509PrivateKey::ProviderType, IX509PrivateKey::get_ProviderType, IX509PrivateKey::put_ProviderType, ProviderType property [Security], ProviderType property [Security],IX509PrivateKey interface, certenroll/IX509PrivateKey::ProviderType, certenroll/IX509PrivateKey::get_ProviderType, certenroll/IX509PrivateKey::put_ProviderType, get_ProviderType, security.ix509privatekey_providertype
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
- apiref
: 
- COM
: 
- certenroll.h
: 
- IX509PrivateKey.get_ProviderType
: 
---

# IX509PrivateKey::get_ProviderType


## -description


The <b>ProviderType</b> property specifies or retrieves the type of cryptographic provider associated with the <a href="https://msdn.microsoft.com/en-us/library/ms721603(v=VS.85).aspx">private key</a>. This property is web enabled for both input and output.

This property is read/write.


## -parameters


## -remarks



You can use this property to force the use of the default provider for a given provider type. For example, to use the <b>PROV_RSA_SCHANNEL</b> provider, set this property to the <b>XCN_PROV_RSA_SCHANNEL</b><a href="https://msdn.microsoft.com/en-us/library/Aa379427(v=VS.85).aspx">X509ProviderType</a> enumeration value and do not specify a value for the <a href="https://msdn.microsoft.com/en-us/library/Aa379031(v=VS.85).aspx">ProviderName</a> property.

Setting this property automatically sets the following properties to be consistent with the specified <b>ProviderType</b> value:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa379022(v=VS.85).aspx">LegacyCsp</a>
</li>
</ul>
These properties are set in the following manner:

<ul>
<li>If the <b>ProviderType</b> is set to <b>XCN_PROV_NONE</b>:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa379022(v=VS.85).aspx">LegacyCsp</a> property is set to <b>VARIANT_FALSE</b>.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a> property is set to <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
<li>If the <b>ProviderType</b> is not set to <b>XCN_PROV_NONE</b>:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa379022(v=VS.85).aspx">LegacyCsp</a> property is set to <b>VARIANT_TRUE</b>.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a> property is set to <b>XCN_AT_SIGNATURE</b> if the  current value is <b>XCN_AT_NONE</b>.</li>
</ul>
</li>
</ul>
Because  a previously specified <a href="https://msdn.microsoft.com/en-us/library/Aa379031(v=VS.85).aspx">ProviderName</a> is not affected by setting the <b>ProviderType</b> property, setting a <b>ProviderType</b> that is inconsistent with the <b>ProviderName</b> property will result in undefined behavior, likely a failure when creating or opening a private key. We recommend that you set the <b>ProviderType</b> property only when attempting to force the use of the default provider for the specified type as discussed above.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378921(v=VS.85).aspx">IX509PrivateKey</a>
 

 

