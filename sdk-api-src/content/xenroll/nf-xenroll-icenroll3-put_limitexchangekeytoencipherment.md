---
UID: NF:xenroll.ICEnroll3.put_LimitExchangeKeyToEncipherment
title: ICEnroll3::put_LimitExchangeKeyToEncipherment
author: windows-sdk-content
description: Sets or retrieves a Boolean value that determines whether an AT_KEYEXCHANGE request contains digital signature and nonrepudiation key usages.
old-location: security\icenroll4_limitexchangekeytoencipherment.htm
tech.root: seccrypto
ms.assetid: d8ed3663-bbda-4052-9c72-b00543ca73ab
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CEnroll object [Security],LimitExchangeKeyToEncipherment property, ICEnroll3 interface [Security],LimitExchangeKeyToEncipherment property, ICEnroll3.LimitExchangeKeyToEncipherment, ICEnroll3.put_LimitExchangeKeyToEncipherment, ICEnroll3::get_LimitExchangeKeyToEncipherment, ICEnroll3::put_LimitExchangeKeyToEncipherment, ICEnroll4 interface [Security],LimitExchangeKeyToEncipherment property, ICEnroll4.LimitExchangeKeyToEncipherment, ICEnroll4::LimitExchangeKeyToEncipherment, ICEnroll4::get_LimitExchangeKeyToEncipherment, ICEnroll4::put_LimitExchangeKeyToEncipherment, LimitExchangeKeyToEncipherment property [Security], LimitExchangeKeyToEncipherment property [Security],CEnroll object, LimitExchangeKeyToEncipherment property [Security],ICEnroll3 interface, LimitExchangeKeyToEncipherment property [Security],ICEnroll4 interface, put_LimitExchangeKeyToEncipherment, security.icenroll4_limitexchangekeytoencipherment, xenroll/ICEnroll3::LimitExchangeKeyToEncipherment, xenroll/ICEnroll3::get_LimitExchangeKeyToEncipherment, xenroll/ICEnroll3::put_LimitExchangeKeyToEncipherment, xenroll/ICEnroll4::LimitExchangeKeyToEncipherment, xenroll/ICEnroll4::get_LimitExchangeKeyToEncipherment, xenroll/ICEnroll4::put_LimitExchangeKeyToEncipherment
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
 - ICEnroll4.LimitExchangeKeyToEncipherment
 - ICEnroll4.get_LimitExchangeKeyToEncipherment
 - ICEnroll4.put_LimitExchangeKeyToEncipherment
 - ICEnroll3.LimitExchangeKeyToEncipherment
 - ICEnroll3.get_LimitExchangeKeyToEncipherment
 - ICEnroll3.put_LimitExchangeKeyToEncipherment
 - CEnroll.LimitExchangeKeyToEncipherment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICEnroll3::put_LimitExchangeKeyToEncipherment


## -description


<p class="CCE_Message">[This property is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>LimitExchangeKeyToEncipherment</b> property sets or retrieves a Boolean value that determines whether an AT_KEYEXCHANGE request contains <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">digital signature</a> and nonrepudiation key usages.

This property was first introduced in the <a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a> interface.

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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Get the LimitExchangeKeyToEncipherment value.
BOOL       bLimitKey;
HRESULT    hr;
// pEnroll is previously instantiated ICEnroll interface pointer.
hr = pEnroll-&gt;get_LimitExchangeKeyToEncipherment(&amp;bLimitKey);
if (FAILED(hr))
    printf("Failed get_LimitExchangeKeyToEncipherment - %x\n", hr );
else
    printf("LimitExchangeKeyToEncipherment: %s\n",
          ( bLimitKey ? "TRUE" : "FALSE"));

// Set the LimitExchangeKeyToEncipherment value.
hr = pEnroll-&gt;put_LimitExchangeKeyToEncipherment( TRUE );
if ( FAILED ( hr ) )
    printf("Failed put_LimitExchangeKeyToEncipherment - %x\n", hr );
else
    printf( "LimitExchangeKeyToEncipherment was set to TRUE\n" );</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/7f13549d-811b-496b-abdd-7e52cbc2ed54">CEnroll</a>



<a href="https://msdn.microsoft.com/4caa7e75-0116-4891-8bf2-ede09a05a440">ICEnroll3</a>



<a href="https://msdn.microsoft.com/4e3e3792-aa41-46fe-bf75-26c2b8959f7a">ICEnroll4</a>



<a href="https://msdn.microsoft.com/30cc7c86-29ce-42e9-b9dc-d29f5b5450a5">KeySpec</a>
 

 

