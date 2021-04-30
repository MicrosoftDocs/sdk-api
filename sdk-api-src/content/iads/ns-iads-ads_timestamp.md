---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0007
title: ADS_TIMESTAMP (iads.h)
description: The ADS_TIMESTAMP structure is an ADSI representation of the Timestamp attribute syntax.
helpviewer_keywords: ["*PADS_TIMESTAMP","ADS_TIMESTAMP","ADS_TIMESTAMP structure [ADSI]","PADS_TIMESTAMP","PADS_TIMESTAMP structure pointer [ADSI]","_ds_ads_timestamp","adsi.ads__timestamp","adsi.ads_timestamp","iads/ADS_TIMESTAMP","iads/PADS_TIMESTAMP"]
old-location: adsi\ads_timestamp.htm
tech.root: adsi
ms.assetid: 3e416a9a-e444-43eb-9e59-e8e91ccac2d9
ms.date: 12/05/2018
ms.keywords: '*PADS_TIMESTAMP, ADS_TIMESTAMP, ADS_TIMESTAMP structure [ADSI], PADS_TIMESTAMP, PADS_TIMESTAMP structure pointer [ADSI], _ds_ads_timestamp, adsi.ads__timestamp, adsi.ads_timestamp, iads/ADS_TIMESTAMP, iads/PADS_TIMESTAMP'
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
req.typenames: ADS_TIMESTAMP, *PADS_TIMESTAMP
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0007
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0007
 - PADS_TIMESTAMP
 - iads/PADS_TIMESTAMP
 - ADS_TIMESTAMP
 - iads/ADS_TIMESTAMP
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
 - ADS_TIMESTAMP
---

# ADS_TIMESTAMP structure


## -description

The <b>ADS_TIMESTAMP</b> structure is an ADSI representation of the <b>Timestamp</b> attribute syntax.

## -struct-fields

### -field WholeSeconds

Number of seconds, with zero value being equal to 12:00 AM, January, 1970, UTC.

### -field EventID

An event identifier, in the order of occurrence, within the period specified by <b>WholeSeconds</b>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>