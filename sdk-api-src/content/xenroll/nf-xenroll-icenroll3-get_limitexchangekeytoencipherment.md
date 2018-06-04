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

# ICEnroll3::get_LimitExchangeKeyToEncipherment


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
 

 

