---
UID: NF:encdec.IETFilterConfig.GetSecureChannelObject
title: IETFilterConfig::GetSecureChannelObject (encdec.h)
description: This topic applies to Windows XP Service Pack 1 or later.
helpviewer_keywords: ["GetSecureChannelObject","GetSecureChannelObject method [Microsoft TV Technologies]","GetSecureChannelObject method [Microsoft TV Technologies]","IETFilterConfig interface","IETFilterConfig interface [Microsoft TV Technologies]","GetSecureChannelObject method","IETFilterConfig.GetSecureChannelObject","IETFilterConfig::GetSecureChannelObject","IETFilterConfigGetSecureChannelObject","encdec/IETFilterConfig::GetSecureChannelObject","mstv.ietfilterconfig_getsecurechannelobject"]
old-location: mstv\ietfilterconfig_getsecurechannelobject.htm
tech.root: mstv
ms.assetid: 385f4525-97b0-4973-8b74-a05816e43556
ms.date: 12/05/2018
ms.keywords: GetSecureChannelObject, GetSecureChannelObject method [Microsoft TV Technologies], GetSecureChannelObject method [Microsoft TV Technologies],IETFilterConfig interface, IETFilterConfig interface [Microsoft TV Technologies],GetSecureChannelObject method, IETFilterConfig.GetSecureChannelObject, IETFilterConfig::GetSecureChannelObject, IETFilterConfigGetSecureChannelObject, encdec/IETFilterConfig::GetSecureChannelObject, mstv.ietfilterconfig_getsecurechannelobject
req.header: encdec.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP1 [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IETFilterConfig::GetSecureChannelObject
 - encdec/IETFilterConfig::GetSecureChannelObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - EncDec.h
api_name:
 - IETFilterConfig.GetSecureChannelObject
---

# IETFilterConfig::GetSecureChannelObject


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This topic applies to Windows XP Service Pack 1 or later.
        



The <b>GetSecureChannelObject</b> method retrieves the secure channel object used to encrypt the stream.

## -parameters

### -param ppUnkDRMSecureChannel [out]

Receives a pointer to the secure channel object's <b>IUnknown</b> interface.

## -returns

Returns an <b>HRESULT</b>.

## -remarks

If the method succeeds, the caller must release the <b>IUnknown</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/encdec/nn-encdec-ietfilterconfig">IETFilterConfig Interface</a>