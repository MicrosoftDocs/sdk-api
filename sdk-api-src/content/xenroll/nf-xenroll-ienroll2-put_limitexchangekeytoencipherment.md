---
UID: NF:xenroll.IEnroll2.put_LimitExchangeKeyToEncipherment
title: IEnroll2::put_LimitExchangeKeyToEncipherment (xenroll.h)
description: The LimitExchangeKeyToEncipherment property of IEnroll4 sets or retrieves a Boolean value that determines whether an AT_KEYEXCHANGE request contains digital signature and nonrepudiation key usages. (Put)
helpviewer_keywords: ["IEnroll2 interface [Security]","LimitExchangeKeyToEncipherment property","IEnroll2.LimitExchangeKeyToEncipherment","IEnroll2.put_LimitExchangeKeyToEncipherment","IEnroll2::LimitExchangeKeyToEncipherment","IEnroll2::get_LimitExchangeKeyToEncipherment","IEnroll2::put_LimitExchangeKeyToEncipherment","IEnroll4 interface [Security]","LimitExchangeKeyToEncipherment property","IEnroll4.LimitExchangeKeyToEncipherment","IEnroll4::get_LimitExchangeKeyToEncipherment","IEnroll4::put_LimitExchangeKeyToEncipherment","LimitExchangeKeyToEncipherment property [Security]","LimitExchangeKeyToEncipherment property [Security]","IEnroll2 interface","LimitExchangeKeyToEncipherment property [Security]","IEnroll4 interface","get_LimitExchangeKeyToEncipherment","put_LimitExchangeKeyToEncipherment","security.ienroll4_limitexchangekeytoencipherment","xenroll/IEnroll2::LimitExchangeKeyToEncipherment","xenroll/IEnroll2::get_LimitExchangeKeyToEncipherment","xenroll/IEnroll2::put_LimitExchangeKeyToEncipherment","xenroll/IEnroll4::LimitExchangeKeyToEncipherment","xenroll/IEnroll4::get_LimitExchangeKeyToEncipherment","xenroll/IEnroll4::put_LimitExchangeKeyToEncipherment"]
old-location: security\ienroll4_limitexchangekeytoencipherment.htm
tech.root: security
ms.assetid: 53d23dcb-081f-44f4-823f-e3cf79955bc3
ms.date: 12/05/2018
ms.keywords: IEnroll2 interface [Security],LimitExchangeKeyToEncipherment property, IEnroll2.LimitExchangeKeyToEncipherment, IEnroll2.put_LimitExchangeKeyToEncipherment, IEnroll2::LimitExchangeKeyToEncipherment, IEnroll2::get_LimitExchangeKeyToEncipherment, IEnroll2::put_LimitExchangeKeyToEncipherment, IEnroll4 interface [Security],LimitExchangeKeyToEncipherment property, IEnroll4.LimitExchangeKeyToEncipherment, IEnroll4::get_LimitExchangeKeyToEncipherment, IEnroll4::put_LimitExchangeKeyToEncipherment, LimitExchangeKeyToEncipherment property [Security], LimitExchangeKeyToEncipherment property [Security],IEnroll2 interface, LimitExchangeKeyToEncipherment property [Security],IEnroll4 interface, get_LimitExchangeKeyToEncipherment, put_LimitExchangeKeyToEncipherment, security.ienroll4_limitexchangekeytoencipherment, xenroll/IEnroll2::LimitExchangeKeyToEncipherment, xenroll/IEnroll2::get_LimitExchangeKeyToEncipherment, xenroll/IEnroll2::put_LimitExchangeKeyToEncipherment, xenroll/IEnroll4::LimitExchangeKeyToEncipherment, xenroll/IEnroll4::get_LimitExchangeKeyToEncipherment, xenroll/IEnroll4::put_LimitExchangeKeyToEncipherment
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnroll2::put_LimitExchangeKeyToEncipherment
 - xenroll/IEnroll2::put_LimitExchangeKeyToEncipherment
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - IEnroll2.LimitExchangeKeyToEncipherment
 - IEnroll2.get_LimitExchangeKeyToEncipherment
 - IEnroll2.put_LimitExchangeKeyToEncipherment
 - IEnroll4.LimitExchangeKeyToEncipherment
 - IEnroll4.get_LimitExchangeKeyToEncipherment
 - IEnroll4.put_LimitExchangeKeyToEncipherment
---

# IEnroll2::put_LimitExchangeKeyToEncipherment


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>LimitExchangeKeyToEncipherment</b> property sets or retrieves a Boolean value that determines whether an AT_KEYEXCHANGE request contains <a href="/windows/desktop/SecGloss/d-gly">digital signature</a> and nonrepudiation key usages.

This property was first introduced in the <a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a> interface.

This property is read/write.

## -parameters

## -remarks

This property is a Boolean value and affects only AT_KEYEXCHANGE requests. It has no impact on AT_SIGNATURE requests.


If the value for this property is <b>FALSE</b>, an AT_KEYEXCHANGE request will contain the following key usages:

<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
</ul>



If the value for this property is <b>TRUE</b>, an AT_KEYEXCHANGE request will contain the following key usages:

<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
</ul>

## -see-also

<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll2">IEnroll2</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-ienroll4">IEnroll4</a>
