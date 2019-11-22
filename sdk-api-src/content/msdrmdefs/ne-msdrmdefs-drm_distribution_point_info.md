---
UID: NE:msdrmdefs._DRM_DISTRIBUTION_POINT_INFO
title: DRM_DISTRIBUTION_POINT_INFO (msdrmdefs.h)

description: Specifies the type of distribution point to retrieve information about when calling DRMGetIssuanceLicenseInfo.
old-location: rm\drm_distribution_point_info.htm
tech.root: AdRms_Sdk
ms.assetid: 09e586bc-bf0e-4831-be35-f00a6288231e

ms.date: 12/05/2018
ms.keywords: DRM_DISTRIBUTION_POINT_INFO, DRM_DISTRIBUTION_POINT_INFO enumeration [Active Directory Rights Management Services SDK 1.0], DRM_DISTRIBUTION_POINT_LICENSE_ACQUISITION, DRM_DISTRIBUTION_POINT_PUBLISHING, DRM_DISTRIBUTION_POINT_REFERRAL_INFO, msdrmdefs/DRM_DISTRIBUTION_POINT_INFO, msdrmdefs/DRM_DISTRIBUTION_POINT_LICENSE_ACQUISITION, msdrmdefs/DRM_DISTRIBUTION_POINT_PUBLISHING, msdrmdefs/DRM_DISTRIBUTION_POINT_REFERRAL_INFO, rm.drm_distribution_point_info, rm.drm_distributionpoint_info
ms.topic: enum
f1_keywords: 
 - "msdrmdefs/DRM_DISTRIBUTION_POINT_INFO"
dev_langs:
 - c++
req.header: msdrmdefs.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRM_DISTRIBUTION_POINT_INFO
targetos: Windows
req.typenames: DRM_DISTRIBUTION_POINT_INFO
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
---

# DRM_DISTRIBUTION_POINT_INFO enumeration


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://docs.microsoft.com/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRM_DISTRIBUTION_POINT_INFO</b> enumeration specifies the type of distribution point to retrieve information about when calling <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetissuancelicenseinfo">DRMGetIssuanceLicenseInfo</a>.


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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/adrms_sdk/ad-rms-enumerations">AD RMS Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetissuancelicenseinfo">DRMGetIssuanceLicenseInfo</a>
 

 

