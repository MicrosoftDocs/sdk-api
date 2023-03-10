---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0048_0006
title: ADS_SD_REVISION_ENUM (iads.h)
description: Specifies the revision number of the access-control entry (ACE), or the access-control list (ACL), for Active Directory.
helpviewer_keywords: ["ADS_SD_REVISION_DS","ADS_SD_REVISION_ENUM","ADS_SD_REVISION_ENUM enumeration [ADSI]","_ds_ads_sd_revision_enum","adsi.ads__sd__revision__enum","adsi.ads_sd_revision_enum","iads/ADS_SD_REVISION_DS","iads/ADS_SD_REVISION_ENUM"]
old-location: adsi\ads_sd_revision_enum.htm
tech.root: adsi
ms.assetid: 3a8c7b5c-5846-4f50-88d2-5a9c86b15480
ms.date: 12/05/2018
ms.keywords: ADS_SD_REVISION_DS, ADS_SD_REVISION_ENUM, ADS_SD_REVISION_ENUM enumeration [ADSI], _ds_ads_sd_revision_enum, adsi.ads__sd__revision__enum, adsi.ads_sd_revision_enum, iads/ADS_SD_REVISION_DS, iads/ADS_SD_REVISION_ENUM
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
req.typenames: ADS_SD_REVISION_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0048_0006
 - iads/__MIDL___MIDL_itf_ads_0001_0048_0006
 - ADS_SD_REVISION_ENUM
 - iads/ADS_SD_REVISION_ENUM
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
 - ADS_SD_REVISION_ENUM
---

# ADS_SD_REVISION_ENUM enumeration


## -description

The <b>ADS_SD_REVISION_ENUM</b> enumeration specifies the revision number of the access-control entry (ACE), or the access-control list (ACL), for Active Directory.

## -enum-fields

### -field ADS_SD_REVISION_DS:4

The revision number of the ACE, or the ACL, for Active Directory.

## -remarks

The <b>ADS_SD_REVISION_DS</b> flag signifies that the related ACL contains object-specific ACEs.

Because VBScript cannot read data from a type library, VBScript applications cannot recognize the symbolic constants as defined above. Use the numerical constants instead to set the appropriate flags in your VBScript applications. To use the symbolic constants as a good programming practice, write explicit declarations of such constants, as done here, in your VBScript applications.

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>
