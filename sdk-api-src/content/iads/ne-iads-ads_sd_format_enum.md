---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0088_0002
title: ADS_SD_FORMAT_ENUM (iads.h)
description: The ADS_SD_FORMAT_ENUM enumeration specifies the format that the security descriptor of an object will be converted to by the IADsSecurityUtility interface.
helpviewer_keywords: ["ADS_SD_FORMAT_ENUM","ADS_SD_FORMAT_ENUM enumeration [ADSI]","ADS_SD_FORMAT_HEXSTRING","ADS_SD_FORMAT_IID","ADS_SD_FORMAT_RAW","_ds_ads_sd_format_enum","adsi.ads__sd__format__enum","adsi.ads_sd_format_enum","iads/ADS_SD_FORMAT_ENUM","iads/ADS_SD_FORMAT_HEXSTRING","iads/ADS_SD_FORMAT_IID","iads/ADS_SD_FORMAT_RAW"]
old-location: adsi\ads_sd_format_enum.htm
tech.root: adsi
ms.assetid: 503247b6-3119-4514-9831-c8f0ef50c0fa
ms.date: 12/05/2018
ms.keywords: ADS_SD_FORMAT_ENUM, ADS_SD_FORMAT_ENUM enumeration [ADSI], ADS_SD_FORMAT_HEXSTRING, ADS_SD_FORMAT_IID, ADS_SD_FORMAT_RAW, _ds_ads_sd_format_enum, adsi.ads__sd__format__enum, adsi.ads_sd_format_enum, iads/ADS_SD_FORMAT_ENUM, iads/ADS_SD_FORMAT_HEXSTRING, iads/ADS_SD_FORMAT_IID, iads/ADS_SD_FORMAT_RAW
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: ADS_SD_FORMAT_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0088_0002
 - iads/__MIDL___MIDL_itf_ads_0001_0088_0002
 - ADS_SD_FORMAT_ENUM
 - iads/ADS_SD_FORMAT_ENUM
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Iads.h
api_name:
 - ADS_SD_FORMAT_ENUM
---

# ADS_SD_FORMAT_ENUM enumeration


## -description

The <b>ADS_SD_FORMAT_ENUM</b> enumeration specifies the format that the security descriptor of an object will be converted to by the <a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a> interface.

## -enum-fields

### -field ADS_SD_FORMAT_IID:1

Indicates that the security descriptor is to be converted to the <a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a> interface format. If <b>ADS_SD_FORMAT_IID</b> is used as the input format when setting the security descriptor, the variant passed in is expected to be a VT_DISPATCH, where the dispatch pointer supports the <b>IADsSecurityDescriptor</b> interface.

### -field ADS_SD_FORMAT_RAW:2

Indicates that the security descriptor is to be converted to the binary format.

### -field ADS_SD_FORMAT_HEXSTRING:3

Indicates that the security descriptor is to be converted to the hex encoded string format.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_pathtype_enum">ADS_PATHTYPE_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a>



<a href="/windows/desktop/ADSI/security-descriptors-on-files-and-registry-keys">Security Descriptors on Files and Registry Keys</a>
