---
UID: NF:certenroll.ICspStatuses.get_ItemByProvider
title: ICspStatuses::get_ItemByProvider (certenroll.h)
description: Retrieves an ICspStatus object that has the same name as the provider specified on input but identifies an algorithm that supports a different intended key use.
helpviewer_keywords: ["ICspStatuses interface [Security]","ItemByProvider property","ICspStatuses.ItemByProvider","ICspStatuses.get_ItemByProvider","ICspStatuses::ItemByProvider","ICspStatuses::get_ItemByProvider","ItemByProvider property [Security]","ItemByProvider property [Security]","ICspStatuses interface","certenroll/ICspStatuses::ItemByProvider","certenroll/ICspStatuses::get_ItemByProvider","get_ItemByProvider","security.icspstatuses_itembyprovider_property"]
old-location: security\icspstatuses_itembyprovider_property.htm
tech.root: security
ms.assetid: 6f6e29b3-4d20-44dc-9a9c-c68b6631a83f
ms.date: 12/05/2018
ms.keywords: ICspStatuses interface [Security],ItemByProvider property, ICspStatuses.ItemByProvider, ICspStatuses.get_ItemByProvider, ICspStatuses::ItemByProvider, ICspStatuses::get_ItemByProvider, ItemByProvider property [Security], ItemByProvider property [Security],ICspStatuses interface, certenroll/ICspStatuses::ItemByProvider, certenroll/ICspStatuses::get_ItemByProvider, get_ItemByProvider, security.icspstatuses_itembyprovider_property
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICspStatuses::get_ItemByProvider
 - certenroll/ICspStatuses::get_ItemByProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICspStatuses.ItemByProvider
 - ICspStatuses.get_ItemByProvider
---

# ICspStatuses::get_ItemByProvider


## -description

The <b>ItemByProvider</b>  property retrieves an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object that has the same name as the  provider specified on input but identifies an algorithm that supports a different intended key use.

This property is read-only.

## -parameters

## -remarks

The <b>ItemByProvider</b>  property retrieves the <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object that matches the name of the input provider but is associated with a different <a href="/windows/desktop/api/certenroll/ne-certenroll-x509keyspec">X509KeySpec</a> enumeration value. For example, if the input provider has a <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_keyspec">KeySpec</a> value of XCN_AT_KEYEXCHANGE, the <b>ItemByProvider</b> property attempts to find an <b>ICspStatus</b> object for the same provider but with a <b>KeySpec</b> value of XCN_AT_SIGNATURE.

Because the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspinformation-get_keyspec">KeySpec</a> property is only associated with legacy providers, if you specify a Cryptography API: Next Generation (CNG) providers, the <b>ItemByProvider</b>  property returns the same <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> object as that entered.

To use this property to iterate through the collection, perform the following steps:<ul>
<li>Retrieve an <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a> collection by calling the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-getcspstatuses">GetCspStatuses</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509certificaterequestpkcs10-get_cspstatuses">CspStatuses</a> property on the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificaterequestpkcs10">IX509CertificateRequestPkcs10</a> interface.</li>
<li>Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icspstatuses-get_itembyindex">ItemByIndex</a> property to iterate through the collection.</li>
<li>For each <a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatus">ICspStatus</a> element retrieved that contains the provider you are interested in, call <b>ItemByProvider</b>.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icspstatuses">ICspStatuses</a>