---
UID: NF:xenroll.IEnroll2.get_LimitExchangeKeyToEncipherment
title: IEnroll2::get_LimitExchangeKeyToEncipherment
author: windows-sdk-content
description: The LimitExchangeKeyToEncipherment property of IEnroll4 sets or retrieves a Boolean value that determines whether an AT_KEYEXCHANGE request contains digital signature and nonrepudiation key usages.
old-location: security\ienroll4_limitexchangekeytoencipherment.htm
tech.root: SecCrypto
ms.assetid: 53d23dcb-081f-44f4-823f-e3cf79955bc3
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnroll2 interface [Security],LimitExchangeKeyToEncipherment property, IEnroll2.LimitExchangeKeyToEncipherment, IEnroll2.get_LimitExchangeKeyToEncipherment, IEnroll2::LimitExchangeKeyToEncipherment, IEnroll2::get_LimitExchangeKeyToEncipherment, IEnroll2::put_LimitExchangeKeyToEncipherment, IEnroll4 interface [Security],LimitExchangeKeyToEncipherment property, IEnroll4.LimitExchangeKeyToEncipherment, IEnroll4::get_LimitExchangeKeyToEncipherment, IEnroll4::put_LimitExchangeKeyToEncipherment, LimitExchangeKeyToEncipherment property [Security], LimitExchangeKeyToEncipherment property [Security],IEnroll2 interface, LimitExchangeKeyToEncipherment property [Security],IEnroll4 interface, get_LimitExchangeKeyToEncipherment, put_LimitExchangeKeyToEncipherment, security.ienroll4_limitexchangekeytoencipherment, xenroll/IEnroll2::LimitExchangeKeyToEncipherment, xenroll/IEnroll2::get_LimitExchangeKeyToEncipherment, xenroll/IEnroll2::put_LimitExchangeKeyToEncipherment, xenroll/IEnroll4::LimitExchangeKeyToEncipherment, xenroll/IEnroll4::get_LimitExchangeKeyToEncipherment, xenroll/IEnroll4::put_LimitExchangeKeyToEncipherment
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xenroll.h
: 
- IEnroll2.get_LimitExchangeKeyToEncipherment
: 
---

# IEnroll2::get_LimitExchangeKeyToEncipherment


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>LimitExchangeKeyToEncipherment</b> property sets or retrieves a Boolean value that determines whether an AT_KEYEXCHANGE request contains <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">digital signature</a> and nonrepudiation key usages.

This property was first introduced in the <a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a> interface.

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




<a href="https://msdn.microsoft.com/60a28944-35de-4ea2-8523-5634685ac224">IEnroll2</a>



<a href="https://msdn.microsoft.com/133529fb-e02a-41a2-83df-646cbc01dbe9">IEnroll4</a>
 

 

