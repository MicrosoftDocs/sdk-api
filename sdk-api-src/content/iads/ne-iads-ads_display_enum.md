---
UID: NE:iads.__MIDL___MIDL_itf_ads_0001_0078_0003
title: ADS_DISPLAY_ENUM (iads.h)
description: The ADS_DISPLAY_ENUM enumeration specifies how a path is to be displayed.
helpviewer_keywords: ["ADS_DISPLAY_ENUM","ADS_DISPLAY_ENUM enumeration [ADSI]","ADS_DISPLAY_FULL","ADS_DISPLAY_VALUE_ONLY","_ds_ads_display_enum","adsi.ads__display__enum","adsi.ads_display_enum","iads/ADS_DISPLAY_ENUM","iads/ADS_DISPLAY_FULL","iads/ADS_DISPLAY_VALUE_ONLY"]
old-location: adsi\ads_display_enum.htm
tech.root: adsi
ms.assetid: bc57aa4d-99f6-483f-b027-9b66b0c3bad1
ms.date: 12/05/2018
ms.keywords: ADS_DISPLAY_ENUM, ADS_DISPLAY_ENUM enumeration [ADSI], ADS_DISPLAY_FULL, ADS_DISPLAY_VALUE_ONLY, _ds_ads_display_enum, adsi.ads__display__enum, adsi.ads_display_enum, iads/ADS_DISPLAY_ENUM, iads/ADS_DISPLAY_FULL, iads/ADS_DISPLAY_VALUE_ONLY
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
req.typenames: ADS_DISPLAY_ENUM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0001_0078_0003
 - iads/__MIDL___MIDL_itf_ads_0001_0078_0003
 - ADS_DISPLAY_ENUM
 - iads/ADS_DISPLAY_ENUM
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
 - ADS_DISPLAY_ENUM
---

# ADS_DISPLAY_ENUM enumeration


## -description

The <b>ADS_DISPLAY_ENUM</b> enumeration specifies how a path is to be displayed.

## -enum-fields

### -field ADS_DISPLAY_FULL:1

The path  is displayed with both attributes and values. For example, CN=Jeff Smith.

### -field ADS_DISPLAY_VALUE_ONLY:2

The path is displayed with values only. For example, Jeff Smith.

## -remarks

This enumeration is used in  <a href="/windows/desktop/api/iads/nf-iads-iadspathname-setdisplaytype">IADsPathname::SetDisplayType</a> method to specify how a path  is to be displayed.

<div class="alert"><b>Note</b>  Because VBScript cannot read data from a type library, VBScript applications do not understand the symbolic constants as defined above. You should use the numeric constants instead to set the appropriate flags in your VBScript applications. If you want to use the symbolic constants as a good programming practice, you should create explicit declarations of such constants, as done here, in your VBScript applications.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/ADSI/adsi-enumerations">ADSI Enumerations</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspathname-setdisplaytype">IADsPathname::SetDisplayType</a>
