---
UID: NF:certenroll.ICspStatuses.get_ItemByProvider
title: ICspStatuses::get_ItemByProvider
author: windows-driver-content
description: Retrieves an ICspStatus object that has the same name as the provider specified on input but identifies an algorithm that supports a different intended key use.
old-location: security\icspstatuses_itembyprovider_property.htm
old-project: SecCertEnroll
ms.assetid: 6f6e29b3-4d20-44dc-9a9c-c68b6631a83f
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ICspStatuses interface [Security],ItemByProvider property, ICspStatuses.ItemByProvider, ICspStatuses.get_ItemByProvider, ICspStatuses::ItemByProvider, ICspStatuses::get_ItemByProvider, ItemByProvider property [Security], ItemByProvider property [Security],ICspStatuses interface, certenroll/ICspStatuses::ItemByProvider, certenroll/ICspStatuses::get_ItemByProvider, get_ItemByProvider, security.icspstatuses_itembyprovider_property
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
-	ICspStatuses.ItemByProvider
-	ICspStatuses.get_ItemByProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICspStatuses::get_ItemByProvider


## -description


The <b>ItemByProvider</b>  property retrieves an <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object that has the same name as the  provider specified on input but identifies an algorithm that supports a different intended key use.

This property is read-only.


## -parameters


## -remarks



The <b>ItemByProvider</b>  property retrieves the <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object that matches the name of the input provider but is associated with a different <a href="https://msdn.microsoft.com/d677d46c-3b36-4081-a6db-123ac1cef84b">X509KeySpec</a> enumeration value. For example, if the input provider has a <a href="https://msdn.microsoft.com/f66f2f5c-7f50-4be6-973e-844d6cb76f61">KeySpec</a> value of XCN_AT_KEYEXCHANGE, the <b>ItemByProvider</b> property attempts to find an <b>ICspStatus</b> object for the same provider but with a <b>KeySpec</b> value of XCN_AT_SIGNATURE.

Because the <a href="https://msdn.microsoft.com/f66f2f5c-7f50-4be6-973e-844d6cb76f61">KeySpec</a> property is only associated with legacy providers, if you specify a Cryptography API: Next Generation (CNG) providers, the <b>ItemByProvider</b>  property returns the same <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object as that entered.

To use this property to iterate through the collection, perform the following steps:<ul>
<li>Retrieve an <a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a> collection by calling the <a href="https://msdn.microsoft.com/50dc8cc5-21ee-4347-a12a-0d6e62901fbb">GetCspStatuses</a> method or the <a href="https://msdn.microsoft.com/cad6d8f0-f7d6-4ede-96a2-b00159962a1b">CspStatuses</a> property on the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> interface.</li>
<li>Call the <a href="https://msdn.microsoft.com/41ccbe27-165d-42d1-95b4-0b96565818aa">ItemByIndex</a> property to iterate through the collection.</li>
<li>For each <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> element retrieved that contains the provider you are interested in, call <b>ItemByProvider</b>.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/73d0f3a7-7afd-42c9-88db-911531c50137">ICspStatuses</a>
 

 

