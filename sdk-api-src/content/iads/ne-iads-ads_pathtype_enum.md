---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0088_0001
title: ADS_PATHTYPE_ENUM (iads.h)
description: The ADS_PATHTYPE_ENUM enumeration specifies the type of object on which the IADsSecurityUtility interface is going to add or modify a security descriptor.
helpviewer_keywords: ["ADS_PATHTYPE_ENUM","ADS_PATHTYPE_ENUM enumeration [ADSI]","ADS_PATH_FILE","ADS_PATH_FILESHARE","ADS_PATH_REGISTRY","_ds_ads_pathtype_enum","adsi.ads__pathtype__enum","adsi.ads_pathtype_enum","iads/ADS_PATHTYPE_ENUM","iads/ADS_PATH_FILE","iads/ADS_PATH_FILESHARE","iads/ADS_PATH_REGISTRY"]
old-location: adsi\ads_pathtype_enum.htm
tech.root: adsi
ms.assetid: 3ae0ec98-9184-4ab3-b859-39c0d677eb0d
ms.date: 12/05/2018
ms.keywords: ADS_PATHTYPE_ENUM, ADS_PATHTYPE_ENUM enumeration [ADSI], ADS_PATH_FILE, ADS_PATH_FILESHARE, ADS_PATH_REGISTRY, _ds_ads_pathtype_enum, adsi.ads__pathtype__enum, adsi.ads_pathtype_enum, iads/ADS_PATHTYPE_ENUM, iads/ADS_PATH_FILE, iads/ADS_PATH_FILESHARE, iads/ADS_PATH_REGISTRY
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
req.typenames: ADS_PATHTYPE_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0088_0001
 - iads/__MIDL___MIDL_itf_ads_0001_0088_0001
 - ADS_PATHTYPE_ENUM
 - iads/ADS_PATHTYPE_ENUM
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
 - ADS_PATHTYPE_ENUM
---

# ADS_PATHTYPE_ENUM enumeration


## -description

The <b>ADS_PATHTYPE_ENUM</b> enumeration specifies the type of object on which the <a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a> interface is going to add or modify a security descriptor.

## -enum-fields

### -field ADS_PATH_FILE:1

Indicates that the security descriptor will be retrieved or set on a file object.

### -field ADS_PATH_FILESHARE:2

Indicates that the security descriptor will be retrieved or set on a file share object.

### -field ADS_PATH_REGISTRY:3

Indicates that the security descriptor will be retrieved or set on a registry key object.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/win32/api/iads/ne-iads-ads_sd_format_enum">ADS_SD_FORMAT_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadssecurityutility">IADsSecurityUtility</a>



<a href="/windows/desktop/ADSI/security-descriptors-on-files-and-registry-keys">Security Descriptors on Files and Registry Keys</a>
