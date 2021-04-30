---
UID: NE:msdrmdefs._DRM_DISTRIBUTION_POINT_INFO
title: DRM_DISTRIBUTION_POINT_INFO (msdrmdefs.h)
description: Specifies the type of distribution point to retrieve information about when calling DRMGetIssuanceLicenseInfo.
helpviewer_keywords: ["DRM_DISTRIBUTION_POINT_INFO","DRM_DISTRIBUTION_POINT_INFO enumeration [Active Directory Rights Management Services SDK 1.0]","DRM_DISTRIBUTION_POINT_LICENSE_ACQUISITION","DRM_DISTRIBUTION_POINT_PUBLISHING","DRM_DISTRIBUTION_POINT_REFERRAL_INFO","msdrmdefs/DRM_DISTRIBUTION_POINT_INFO","msdrmdefs/DRM_DISTRIBUTION_POINT_LICENSE_ACQUISITION","msdrmdefs/DRM_DISTRIBUTION_POINT_PUBLISHING","msdrmdefs/DRM_DISTRIBUTION_POINT_REFERRAL_INFO","rm.drm_distribution_point_info","rm.drm_distributionpoint_info"]
old-location: rm\drm_distribution_point_info.htm
tech.root: rm
ms.assetid: 09e586bc-bf0e-4831-be35-f00a6288231e
ms.date: 10/15/2020
ms.keywords: DRM_DISTRIBUTION_POINT_INFO, DRM_DISTRIBUTION_POINT_INFO enumeration [Active Directory Rights Management Services SDK 1.0], DRM_DISTRIBUTION_POINT_LICENSE_ACQUISITION, DRM_DISTRIBUTION_POINT_PUBLISHING, DRM_DISTRIBUTION_POINT_REFERRAL_INFO, msdrmdefs/DRM_DISTRIBUTION_POINT_INFO, msdrmdefs/DRM_DISTRIBUTION_POINT_LICENSE_ACQUISITION, msdrmdefs/DRM_DISTRIBUTION_POINT_PUBLISHING, msdrmdefs/DRM_DISTRIBUTION_POINT_REFERRAL_INFO, rm.drm_distribution_point_info, rm.drm_distributionpoint_info
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
targetos: Windows
req.typenames: DRM_DISTRIBUTION_POINT_INFO
req.redist: 
req.product: Rights Management Services client 1.0 SP2 or later
ms.custom: 19H1
f1_keywords:
 - _DRM_DISTRIBUTION_POINT_INFO
 - msdrmdefs/_DRM_DISTRIBUTION_POINT_INFO
 - DRM_DISTRIBUTION_POINT_INFO
 - msdrmdefs/DRM_DISTRIBUTION_POINT_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Msdrmdefs.h
api_name:
 - DRM_DISTRIBUTION_POINT_INFO
---

# DRM_DISTRIBUTION_POINT_INFO enumeration


## -description

> [!NOTE]
> The AD RMS SDK leveraging functionality exposed by the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or unavailable in subsequent versions. Instead, use [Active Directory Rights Management Services SDK 2.1](/previous-versions/windows/desktop/msipc/microsoft-information-protection-and-control-client-portal), which leverages functionality exposed by the client in **Msipc.dll**.

The **DRM_DISTRIBUTION_POINT_INFO** enumeration specifies the type of distribution point to retrieve information about when calling [DRMGetIssuanceLicenseInfo](/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetissuancelicenseinfo).

## -enum-fields

### -field DRM_DISTRIBUTION_POINT_LICENSE_ACQUISITION

Retrieves information about the default end-user license acquisition URL contained in the issuance license. Use this constant to retrieve information about the silent intranet URL. The following example shows a license acquisition URL.

```xml
<DISTRIBUTIONPOINT>
  <OBJECT type="License-Acquisition-URL">
    <ID type="MS-GUID">
       {0045FD50-383B-43AA-90A4-ED013CD0CFE5}
    </ID>
    <NAME>Contoso Licensing Authority</NAME>
    <ADDRESS type="URL">
        http://Contoso.com/_wmcs/licensing
    </ADDRESS>
  </OBJECT>
</DISTRIBUTIONPOINT>
```

### -field DRM_DISTRIBUTION_POINT_PUBLISHING

Retrieves information about the issuance license signing service URL contained in the issuance license. The following example shows a signing service URL.

```xml
<DISTRIBUTIONPOINT>
  <OBJECT type="Publishing-URL">
    <ID type="MS-GUID">{9A23D98E-4449-4ba5-812A-F30808F3CB16}</ID> 
    <NAME>Publishing Point</NAME> 
    <ADDRESS type="URL">HTTP://petx64a526/_wmcs/licensing</ADDRESS> 
  </OBJECT>
</DISTRIBUTIONPOINT>
```

### -field DRM_DISTRIBUTION_POINT_REFERRAL_INFO

Retrieves information about the nonsilent end-user license acquisition URL in the issuance license.

>[!Note]
>Beginning with RMS 1.0 SP1, nonsilent license acquisition is no longer supported.

```xml
<DISTRIBUTIONPOINT>
  <OBJECT type="Referral-Info">
    <ID type="MS-GUID">{81C42010-208A-4ABA-BAB6-C3C60F06DD5F}</ID>
    <NAME>Contoso Credit Card Splash Page</NAME>
    <ADDRESS type="URL">
       https://www.contoso.com/CreditCardOffers.htm
    </ADDRESS>
  </OBJECT>
</DISTRIBUTIONPOINT>
```

## -see-also

[AD RMS Enumerations](/previous-versions/windows/desktop/adrms_sdk/ad-rms-enumerations)

[DRMGetIssuanceLicenseInfo](/previous-versions/windows/desktop/api/msdrm/nf-msdrm-drmgetissuancelicenseinfo)
