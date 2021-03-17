---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0015
title: ADS_DN_WITH_BINARY (iads.h)
description: Used with the ADSVALUE structure to contain a distinguished name attribute value that also contains binary data.
helpviewer_keywords: ["*PADS_DN_WITH_BINARY","ADS_DN_WITH_BINARY","ADS_DN_WITH_BINARY structure [ADSI]","_ds_ads_dn_with_binary","adsi.ads__dn__with__binary","adsi.ads_dn_with_binary","iads/ADS_DN_WITH_BINARY"]
old-location: adsi\ads_dn_with_binary.htm
tech.root: adsi
ms.assetid: 541dd19d-79a1-4a74-b4a1-31cdf69fbf0c
ms.date: 12/05/2018
ms.keywords: '*PADS_DN_WITH_BINARY, ADS_DN_WITH_BINARY, ADS_DN_WITH_BINARY structure [ADSI], _ds_ads_dn_with_binary, adsi.ads__dn__with__binary, adsi.ads_dn_with_binary, iads/ADS_DN_WITH_BINARY'
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
req.typenames: ADS_DN_WITH_BINARY, *PADS_DN_WITH_BINARY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0015
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0015
 - PADS_DN_WITH_BINARY
 - iads/PADS_DN_WITH_BINARY
 - ADS_DN_WITH_BINARY
 - iads/ADS_DN_WITH_BINARY
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
 - ADS_DN_WITH_BINARY
---

# ADS_DN_WITH_BINARY structure


## -description

The <b>ADS_DN_WITH_BINARY</b> structure is used with the <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structure to contain a distinguished name attribute value that also contains binary data.

## -struct-fields

### -field dwLength

Contains the length, in bytes, of the binary data in <b>lpBinaryValue</b>.

### -field lpBinaryValue

Pointer to an array of bytes that contains the binary data for the attribute. The <b>dwLength</b> member contains the number of bytes in this array.

### -field pszDNString

Pointer to a null-terminated Unicode string that contains the distinguished name.

## -remarks

When extending the active directory schema to add <b>ADS_DN_WITH_BINARY</b>, you must also specify the otherWellKnownGuid attribute definition. Add the following to the ldf file attribute definition: omObjectClass:: KoZIhvcUAQEBCw==

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>



<a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a>



<a href="/windows/desktop/ADSchema/s-object-dn-binary">Object(DN-Binary)</a>