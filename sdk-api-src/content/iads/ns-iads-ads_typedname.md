---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0009
title: ADS_TYPEDNAME (iads.h)
description: Represents an ADSI representation of Typed Name attribute syntax.
helpviewer_keywords: ["*PADS_TYPEDNAME","ADS_TYPEDNAME","ADS_TYPEDNAME structure [ADSI]","PADS_TYPEDNAME","PADS_TYPEDNAME structure pointer [ADSI]","_ds_ads_typedname","adsi.ads__typedname","adsi.ads_typedname","iads/ADS_TYPEDNAME","iads/PADS_TYPEDNAME"]
old-location: adsi\ads_typedname.htm
tech.root: adsi
ms.assetid: 64ce748c-adfc-4beb-8507-ca6aece46ad0
ms.date: 12/05/2018
ms.keywords: '*PADS_TYPEDNAME, ADS_TYPEDNAME, ADS_TYPEDNAME structure [ADSI], PADS_TYPEDNAME, PADS_TYPEDNAME structure pointer [ADSI], _ds_ads_typedname, adsi.ads__typedname, adsi.ads_typedname, iads/ADS_TYPEDNAME, iads/PADS_TYPEDNAME'
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
req.typenames: ADS_TYPEDNAME, *PADS_TYPEDNAME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0009
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0009
 - PADS_TYPEDNAME
 - iads/PADS_TYPEDNAME
 - ADS_TYPEDNAME
 - iads/ADS_TYPEDNAME
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
 - ADS_TYPEDNAME
---

# ADS_TYPEDNAME structure


## -description

The <b>ADS_TYPEDNAME</b> structure represents an ADSI representation of <b>Typed Name</b> attribute syntax.

## -struct-fields

### -field ObjectName

The null-terminated Unicode string that contains an object name.

### -field Level

The priority associated with the object.

### -field Interval

The frequency of reference of the object.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>