---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0004
title: ADS_PROV_SPECIFIC (iads.h)
description: The ADS_PROV_SPECIFIC structure contains provider-specific data represented as a binary large object (BLOB).
helpviewer_keywords: ["*PADS_PROV_SPECIFIC","ADS_PROV_SPECIFIC","ADS_PROV_SPECIFIC structure [ADSI]","PADS_PROV_SPECIFIC","PADS_PROV_SPECIFIC structure pointer [ADSI]","_ds_ads_prov_specific","adsi.ads__prov__specific","adsi.ads_prov_specific","iads/ADS_PROV_SPECIFIC","iads/PADS_PROV_SPECIFIC"]
old-location: adsi\ads_prov_specific.htm
tech.root: adsi
ms.assetid: 45927280-7fb5-49a6-8ecd-f0a6931bed6a
ms.date: 12/05/2018
ms.keywords: '*PADS_PROV_SPECIFIC, ADS_PROV_SPECIFIC, ADS_PROV_SPECIFIC structure [ADSI], PADS_PROV_SPECIFIC, PADS_PROV_SPECIFIC structure pointer [ADSI], _ds_ads_prov_specific, adsi.ads__prov__specific, adsi.ads_prov_specific, iads/ADS_PROV_SPECIFIC, iads/PADS_PROV_SPECIFIC'
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
req.typenames: ADS_PROV_SPECIFIC, *PADS_PROV_SPECIFIC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0004
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0004
 - PADS_PROV_SPECIFIC
 - iads/PADS_PROV_SPECIFIC
 - ADS_PROV_SPECIFIC
 - iads/ADS_PROV_SPECIFIC
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
 - ADS_PROV_SPECIFIC
---

# ADS_PROV_SPECIFIC structure


## -description

The <b>ADS_PROV_SPECIFIC</b> structure contains provider-specific data represented as a binary large object (BLOB).

## -struct-fields

### -field dwLength

The size of the character array.

### -field lpValue

A pointer to an array of bytes.

## -remarks

The <b>ADS_PROV_SPECIFIC</b> structure is one of the data types used as a member of the  <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structure definition. The data is represented as a BLOB here, although the actual data can be packed in any format, such as a C structure. The provider writer must publish the specific data format under the BLOB.

ADSI may also return attributes as <b>ADS_PROV_SPECIFIC</b> if unable to determine the correct attribute syntax type as would occur if, for example, the schema was unavailable.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>



<a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a>