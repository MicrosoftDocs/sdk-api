---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0002
title: ADS_OCTET_STRING (iads.h)
description: The ADS_OCTET_STRING structure is an ADSI representation of the Octet String attribute syntax used in Active Directory.
helpviewer_keywords: ["*PADS_OCTET_STRING","ADS_OCTET_STRING","ADS_OCTET_STRING structure [ADSI]","PADS_OCTET_STRING","PADS_OCTET_STRING structure pointer [ADSI]","_ds_ads_octet_string","adsi.ads__octet__string","adsi.ads_octet_string","iads/ADS_OCTET_STRING","iads/PADS_OCTET_STRING"]
old-location: adsi\ads_octet_string.htm
tech.root: adsi
ms.assetid: ecad3601-081d-4cb6-a6dd-7781d652af8e
ms.date: 12/05/2018
ms.keywords: '*PADS_OCTET_STRING, ADS_OCTET_STRING, ADS_OCTET_STRING structure [ADSI], PADS_OCTET_STRING, PADS_OCTET_STRING structure pointer [ADSI], _ds_ads_octet_string, adsi.ads__octet__string, adsi.ads_octet_string, iads/ADS_OCTET_STRING, iads/PADS_OCTET_STRING'
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
req.typenames: ADS_OCTET_STRING, *PADS_OCTET_STRING
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0002
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0002
 - PADS_OCTET_STRING
 - iads/PADS_OCTET_STRING
 - ADS_OCTET_STRING
 - iads/ADS_OCTET_STRING
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
 - ADS_OCTET_STRING
---

# ADS_OCTET_STRING structure


## -description

The <b>ADS_OCTET_STRING</b> structure is an ADSI representation of the <b>Octet String</b> attribute syntax used in Active Directory.

## -struct-fields

### -field dwLength

The size, in bytes, of the character array.

### -field lpValue

Pointer to an array of single byte characters 
not interpreted by the underlying directory.

## -remarks

Memory for the byte array must be allocated separately.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>