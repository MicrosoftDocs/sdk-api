---
UID: NF:xenroll.ICEnroll3.get_LimitExchangeKeyToEncipherment
title: ICEnroll3::get_LimitExchangeKeyToEncipherment (xenroll.h)
description: Sets or retrieves a Boolean value that determines whether an AT_KEYEXCHANGE request contains digital signature and nonrepudiation key usages. (Get)
helpviewer_keywords: ["CEnroll object [Security]","LimitExchangeKeyToEncipherment property","ICEnroll3 interface [Security]","LimitExchangeKeyToEncipherment property","ICEnroll3.LimitExchangeKeyToEncipherment","ICEnroll3.get_LimitExchangeKeyToEncipherment","ICEnroll3::get_LimitExchangeKeyToEncipherment","ICEnroll3::put_LimitExchangeKeyToEncipherment","ICEnroll4 interface [Security]","LimitExchangeKeyToEncipherment property","ICEnroll4.LimitExchangeKeyToEncipherment","ICEnroll4::LimitExchangeKeyToEncipherment","ICEnroll4::get_LimitExchangeKeyToEncipherment","ICEnroll4::put_LimitExchangeKeyToEncipherment","LimitExchangeKeyToEncipherment property [Security]","LimitExchangeKeyToEncipherment property [Security]","CEnroll object","LimitExchangeKeyToEncipherment property [Security]","ICEnroll3 interface","LimitExchangeKeyToEncipherment property [Security]","ICEnroll4 interface","get_LimitExchangeKeyToEncipherment","security.icenroll4_limitexchangekeytoencipherment","xenroll/ICEnroll3::LimitExchangeKeyToEncipherment","xenroll/ICEnroll3::get_LimitExchangeKeyToEncipherment","xenroll/ICEnroll3::put_LimitExchangeKeyToEncipherment","xenroll/ICEnroll4::LimitExchangeKeyToEncipherment","xenroll/ICEnroll4::get_LimitExchangeKeyToEncipherment","xenroll/ICEnroll4::put_LimitExchangeKeyToEncipherment"]
old-location: security\icenroll4_limitexchangekeytoencipherment.htm
tech.root: security
ms.assetid: d8ed3663-bbda-4052-9c72-b00543ca73ab
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],LimitExchangeKeyToEncipherment property, ICEnroll3 interface [Security],LimitExchangeKeyToEncipherment property, ICEnroll3.LimitExchangeKeyToEncipherment, ICEnroll3.get_LimitExchangeKeyToEncipherment, ICEnroll3::get_LimitExchangeKeyToEncipherment, ICEnroll3::put_LimitExchangeKeyToEncipherment, ICEnroll4 interface [Security],LimitExchangeKeyToEncipherment property, ICEnroll4.LimitExchangeKeyToEncipherment, ICEnroll4::LimitExchangeKeyToEncipherment, ICEnroll4::get_LimitExchangeKeyToEncipherment, ICEnroll4::put_LimitExchangeKeyToEncipherment, LimitExchangeKeyToEncipherment property [Security], LimitExchangeKeyToEncipherment property [Security],CEnroll object, LimitExchangeKeyToEncipherment property [Security],ICEnroll3 interface, LimitExchangeKeyToEncipherment property [Security],ICEnroll4 interface, get_LimitExchangeKeyToEncipherment, security.icenroll4_limitexchangekeytoencipherment, xenroll/ICEnroll3::LimitExchangeKeyToEncipherment, xenroll/ICEnroll3::get_LimitExchangeKeyToEncipherment, xenroll/ICEnroll3::put_LimitExchangeKeyToEncipherment, xenroll/ICEnroll4::LimitExchangeKeyToEncipherment, xenroll/ICEnroll4::get_LimitExchangeKeyToEncipherment, xenroll/ICEnroll4::put_LimitExchangeKeyToEncipherment
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
 - ICEnroll3::get_LimitExchangeKeyToEncipherment
 - xenroll/ICEnroll3::get_LimitExchangeKeyToEncipherment
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
 - ICEnroll4.LimitExchangeKeyToEncipherment
 - ICEnroll4.get_LimitExchangeKeyToEncipherment
 - ICEnroll4.put_LimitExchangeKeyToEncipherment
 - ICEnroll3.LimitExchangeKeyToEncipherment
 - ICEnroll3.get_LimitExchangeKeyToEncipherment
 - ICEnroll3.put_LimitExchangeKeyToEncipherment
 - CEnroll.LimitExchangeKeyToEncipherment
---

# ICEnroll3::get_LimitExchangeKeyToEncipherment


## -description

<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>LimitExchangeKeyToEncipherment</b> property sets or retrieves a Boolean value that determines whether an AT_KEYEXCHANGE request contains <a href="/windows/desktop/SecGloss/d-gly">digital signature</a> and nonrepudiation key usages.

This property was first introduced in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a> interface.

This property is read/write.

## -parameters

## -remarks

This property is a Boolean value and affects only AT_KEYEXCHANGE requests. It has no impact on AT_SIGNATURE requests.


If the value for this property is false, an AT_KEYEXCHANGE request will contain the following key usages:

<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
</ul>



If the value for this property is true, an AT_KEYEXCHANGE request will contain the following key usages:

<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
</ul>



#### Examples


```cpp
// Get the LimitExchangeKeyToEncipherment value.
BOOL       bLimitKey;
HRESULT    hr;
// pEnroll is previously instantiated ICEnroll interface pointer.
hr = pEnroll->get_LimitExchangeKeyToEncipherment(&bLimitKey);
if (FAILED(hr))
    printf("Failed get_LimitExchangeKeyToEncipherment - %x\n", hr );
else
    printf("LimitExchangeKeyToEncipherment: %s\n",
          ( bLimitKey ? "TRUE" : "FALSE"));

// Set the LimitExchangeKeyToEncipherment value.
hr = pEnroll->put_LimitExchangeKeyToEncipherment( TRUE );
if ( FAILED ( hr ) )
    printf("Failed put_LimitExchangeKeyToEncipherment - %x\n", hr );
else
    printf( "LimitExchangeKeyToEncipherment was set to TRUE\n" );
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_keyspec">KeySpec</a>
