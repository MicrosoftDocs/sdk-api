---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0013
title: ADS_FAXNUMBER (iads.h)
description: The ADS_FAXNUMBER structure is an ADSI representation of the Facsimile Telephone Number attribute syntax.
helpviewer_keywords: ["*PADS_FAXNUMBER","ADS_FAXNUMBER","ADS_FAXNUMBER structure [ADSI]","PADS_FAXNUMBER","PADS_FAXNUMBER structure pointer [ADSI]","_ds_ads_faxnumber","adsi.ads__faxnumber","adsi.ads_faxnumber","iads/ADS_FAXNUMBER","iads/PADS_FAXNUMBER"]
old-location: adsi\ads_faxnumber.htm
tech.root: adsi
ms.assetid: 32553290-e9ca-44e7-a085-f053df8104e6
ms.date: 12/05/2018
ms.keywords: '*PADS_FAXNUMBER, ADS_FAXNUMBER, ADS_FAXNUMBER structure [ADSI], PADS_FAXNUMBER, PADS_FAXNUMBER structure pointer [ADSI], _ds_ads_faxnumber, adsi.ads__faxnumber, adsi.ads_faxnumber, iads/ADS_FAXNUMBER, iads/PADS_FAXNUMBER'
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
req.typenames: ADS_FAXNUMBER, *PADS_FAXNUMBER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0013
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0013
 - PADS_FAXNUMBER
 - iads/PADS_FAXNUMBER
 - ADS_FAXNUMBER
 - iads/ADS_FAXNUMBER
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
 - ADS_FAXNUMBER
---

# ADS_FAXNUMBER structure


## -description

The <b>ADS_FAXNUMBER</b> structure is an ADSI representation of the <b>Facsimile Telephone Number</b> attribute syntax.

## -struct-fields

### -field TelephoneNumber

The null-terminated Unicode string value that contains the telephone number of the facsimile (fax) machine.

### -field NumberOfBits

The number of data bits.

### -field Parameters

Optional parameters for the fax machine.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>