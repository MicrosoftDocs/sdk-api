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

# _DRM_DISTRIBUTION_POINT_INFO enumeration


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRM_DISTRIBUTION_POINT_INFO</b> enumeration specifies the type of distribution point to retrieve information about when calling <a href="https://msdn.microsoft.com/67213b97-3831-4284-b807-f6bc69d4b610">DRMGetIssuanceLicenseInfo</a>.


## -enum-fields




### -field DRM_DISTRIBUTION_POINT_LICENSE_ACQUISITION

Retrieves information about the default end-user license acquisition URL contained in the issuance license. Use this constant to retrieve information about the silent intranet URL. The following example shows a license acquisition URL.

<pre class="syntax" xml:space="preserve"><code>&lt;DISTRIBUTIONPOINT&gt;
  &lt;OBJECT type="License-Acquisition-URL"&gt;
    &lt;ID type="MS-GUID"&gt;
       {0045FD50-383B-43AA-90A4-ED013CD0CFE5}
    &lt;/ID&gt;
    &lt;NAME&gt;Contoso Licensing Authority&lt;/NAME&gt;
    &lt;ADDRESS type="URL"&gt;
        http://Contoso.com/_wmcs/licensing
    &lt;/ADDRESS&gt;
  &lt;/OBJECT&gt;
&lt;/DISTRIBUTIONPOINT&gt;</code></pre>

### -field DRM_DISTRIBUTION_POINT_PUBLISHING

Retrieves information about the issuance license signing service URL contained in the issuance license. The following example shows a signing service URL.

<pre class="syntax" xml:space="preserve"><code>&lt;DISTRIBUTIONPOINT&gt;
  &lt;OBJECT type="Publishing-URL"&gt;
    &lt;ID type="MS-GUID"&gt;{9A23D98E-4449-4ba5-812A-F30808F3CB16}&lt;/ID&gt; 
    &lt;NAME&gt;Publishing Point&lt;/NAME&gt; 
    &lt;ADDRESS type="URL"&gt;HTTP://petx64a526/_wmcs/licensing&lt;/ADDRESS&gt; 
  &lt;/OBJECT&gt;
&lt;/DISTRIBUTIONPOINT&gt;</code></pre>

### -field DRM_DISTRIBUTION_POINT_REFERRAL_INFO

Retrieves information about the nonsilent end-user   license acquisition URL in the issuance license.<div class="alert"><b>Note</b>  Beginning with RMS 1.0 SP1, nonsilent license acquisition is no longer supported.</div>
<div> </div>


<pre class="syntax" xml:space="preserve"><code>&lt;DISTRIBUTIONPOINT&gt;
  &lt;OBJECT type="Referral-Info"&gt;
    &lt;ID type="MS-GUID"&gt;{81C42010-208A-4ABA-BAB6-C3C60F06DD5F}&lt;/ID&gt;
    &lt;NAME&gt;Contoso Credit Card Splash Page&lt;/NAME&gt;
    &lt;ADDRESS type="URL"&gt;
       https://www.contoso.com/CreditCardOffers.htm
    &lt;/ADDRESS&gt;
  &lt;/OBJECT&gt;
&lt;/DISTRIBUTIONPOINT&gt;</code></pre>

## -see-also




<a href="https://msdn.microsoft.com/bc3a8ab3-9f89-442b-9910-85820b2b2653">AD RMS Enumerations</a>



<a href="https://msdn.microsoft.com/67213b97-3831-4284-b807-f6bc69d4b610">DRMGetIssuanceLicenseInfo</a>
 

 

