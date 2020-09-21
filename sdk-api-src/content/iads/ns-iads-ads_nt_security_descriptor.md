---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0003
title: ADS_NT_SECURITY_DESCRIPTOR (iads.h)
description: The ADS_NT_SECURITY_DESCRIPTOR structure defines the data type of the security descriptor for Windows.
helpviewer_keywords: ["*PADS_NT_SECURITY_DESCRIPTOR","ADS_NT_SECURITY_DESCRIPTOR","ADS_NT_SECURITY_DESCRIPTOR structure [ADSI]","PADS_NT_SECURITY_DESCRIPTOR","PADS_NT_SECURITY_DESCRIPTOR structure pointer [ADSI]","_ds_ads_nt_security_descriptor","adsi.ads__nt__security__descriptor","adsi.ads_nt_security_descriptor","iads/ADS_NT_SECURITY_DESCRIPTOR","iads/PADS_NT_SECURITY_DESCRIPTOR"]
old-location: adsi\ads_nt_security_descriptor.htm
tech.root: adsi
ms.assetid: 4776fe35-2c16-4dd3-b708-cf36e2423425
ms.date: 12/05/2018
ms.keywords: '*PADS_NT_SECURITY_DESCRIPTOR, ADS_NT_SECURITY_DESCRIPTOR, ADS_NT_SECURITY_DESCRIPTOR structure [ADSI], PADS_NT_SECURITY_DESCRIPTOR, PADS_NT_SECURITY_DESCRIPTOR structure pointer [ADSI], _ds_ads_nt_security_descriptor, adsi.ads__nt__security__descriptor, adsi.ads_nt_security_descriptor, iads/ADS_NT_SECURITY_DESCRIPTOR, iads/PADS_NT_SECURITY_DESCRIPTOR'
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
req.typenames: ADS_NT_SECURITY_DESCRIPTOR, *PADS_NT_SECURITY_DESCRIPTOR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0003
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0003
 - PADS_NT_SECURITY_DESCRIPTOR
 - iads/PADS_NT_SECURITY_DESCRIPTOR
 - ADS_NT_SECURITY_DESCRIPTOR
 - iads/ADS_NT_SECURITY_DESCRIPTOR
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
 - ADS_NT_SECURITY_DESCRIPTOR
---

# ADS_NT_SECURITY_DESCRIPTOR structure


## -description

The <b>ADS_NT_SECURITY_DESCRIPTOR</b> structure defines the data type of the security descriptor for Windows.

## -struct-fields

### -field dwLength

The length data, in bytes.

### -field lpValue

Pointer to the security descriptor, represented as a byte array.

## -remarks

The <b>ADS_NT_SECURITY_DESCRIPTOR</b> structure is normally used as a member of the <a href="/windows/desktop/api/iads/ns-iads-adsvalue">ADSVALUE</a> structure definition.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>