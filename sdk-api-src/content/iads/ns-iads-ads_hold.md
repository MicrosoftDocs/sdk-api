---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0010
title: ADS_HOLD (iads.h)
description: The ADS_HOLD structure is an ADSI representation of the Hold attribute syntax.
helpviewer_keywords: ["*PADS_HOLD","ADS_HOLD","ADS_HOLD structure [ADSI]","PADS_HOLD","PADS_HOLD structure pointer [ADSI]","_ds_ads_hold","adsi.ads__hold","adsi.ads_hold","iads/ADS_HOLD","iads/PADS_HOLD"]
old-location: adsi\ads_hold.htm
tech.root: adsi
ms.assetid: f1ef87f0-b024-4d16-873b-a68bb62f4206
ms.date: 12/05/2018
ms.keywords: '*PADS_HOLD, ADS_HOLD, ADS_HOLD structure [ADSI], PADS_HOLD, PADS_HOLD structure pointer [ADSI], _ds_ads_hold, adsi.ads__hold, adsi.ads_hold, iads/ADS_HOLD, iads/PADS_HOLD'
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
req.typenames: ADS_HOLD, *PADS_HOLD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0010
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0010
 - PADS_HOLD
 - iads/PADS_HOLD
 - ADS_HOLD
 - iads/ADS_HOLD
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
 - ADS_HOLD
---

# ADS_HOLD structure


## -description

The <b>ADS_HOLD</b> structure is an ADSI representation of the <b>Hold</b> attribute syntax.

## -struct-fields

### -field ObjectName

The null-terminated Unicode string that contains the name of an object put on hold.

### -field Amount

Number of charges that a server places against the user on hold while it verifies the user account balance.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>