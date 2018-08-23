---
UID: NF:certenroll.IX509AttributeCspProvider.get_Signature
title: IX509AttributeCspProvider::get_Signature
author: windows-sdk-content
description: Retrieves the digital signature on the provider.
old-location: security\ix509attributecspprovider_signature_property.htm
old-project: seccertenroll
ms.assetid: 06245293-b331-4963-a0cf-b7c604580908
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509AttributeCspProvider interface [Security],Signature property, IX509AttributeCspProvider.Signature, IX509AttributeCspProvider.get_Signature, IX509AttributeCspProvider::Signature, IX509AttributeCspProvider::get_Signature, Signature property [Security], Signature property [Security],IX509AttributeCspProvider interface, certenroll/IX509AttributeCspProvider::Signature, certenroll/IX509AttributeCspProvider::get_Signature, get_Signature, security.ix509attributecspprovider_signature_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509AttributeCspProvider::get_Signature


## -description


The <b>Signature</b> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">digital signature</a> on the provider. The signature is contained in a byte array represented by a Unicode-encoded string.

This property is read-only.


## -parameters


## -remarks



Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377084(v=VS.85).aspx">InitializeEncode</a> method or the  <a href="https://msdn.microsoft.com/en-us/library/Aa377083(v=VS.85).aspx">InitializeDecode</a> method to initialize the <b>Signature</b> property. You can call the following properties to retrieve the raw data:

<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377085(v=VS.85).aspx">KeySpec</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377088(v=VS.85).aspx">ProviderName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa377082(v=VS.85).aspx">IX509AttributeCspProvider</a>
 

 

