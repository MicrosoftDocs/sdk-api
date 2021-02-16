---
UID: NS:iads.__MIDL___MIDL_itf_ads_0000_0000_0008
title: ADS_BACKLINK (iads.h)
description: The ADS_BACKLINK structure is an ADSI representation of the Back Link attribute syntax.
helpviewer_keywords: ["*PADS_BACKLINK","ADS_BACKLINK","ADS_BACKLINK structure [ADSI]","PADS_BACKLINK","PADS_BACKLINK structure pointer [ADSI]","_ds_ads_backlink","adsi.ads__backlink","adsi.ads_backlink","iads/ADS_BACKLINK","iads/PADS_BACKLINK"]
old-location: adsi\ads_backlink.htm
tech.root: adsi
ms.assetid: 1352d304-b984-43ab-8c47-5108f35ae193
ms.date: 12/05/2018
ms.keywords: '*PADS_BACKLINK, ADS_BACKLINK, ADS_BACKLINK structure [ADSI], PADS_BACKLINK, PADS_BACKLINK structure pointer [ADSI], _ds_ads_backlink, adsi.ads__backlink, adsi.ads_backlink, iads/ADS_BACKLINK, iads/PADS_BACKLINK'
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
req.typenames: ADS_BACKLINK, *PADS_BACKLINK
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_ads_0000_0000_0008
 - iads/__MIDL___MIDL_itf_ads_0000_0000_0008
 - PADS_BACKLINK
 - iads/PADS_BACKLINK
 - ADS_BACKLINK
 - iads/ADS_BACKLINK
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
 - ADS_BACKLINK
---

# ADS_BACKLINK structure


## -description

The <b>ADS_BACKLINK</b> structure is an ADSI representation of the <b>Back Link</b> attribute syntax.

## -struct-fields

### -field RemoteID

Identifier of the remote server that requires an external reference to the object specified by <b>ObjectName</b>. See below.

### -field ObjectName

The null-terminated Unicode string that specifies the name of an object to which the <b>Back Link</b> attribute is attached.

## -remarks

A <b>Back Link</b> attribute contains one or more servers that hold an external reference to the attached object.

## -see-also

<a href="/windows/desktop/ADSI/adsi-structures">ADSI Structures</a>