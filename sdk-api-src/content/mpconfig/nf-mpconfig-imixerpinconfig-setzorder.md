---
UID: NF:mpconfig.IMixerPinConfig.SetZOrder
title: IMixerPinConfig::SetZOrder (mpconfig.h)
description: The SetZOrder method sets the z-order of a particular video stream.
helpviewer_keywords: ["IMixerPinConfig interface [DirectShow]","SetZOrder method","IMixerPinConfig.SetZOrder","IMixerPinConfig::SetZOrder","IMixerPinConfigSetZOrder","SetZOrder","SetZOrder method [DirectShow]","SetZOrder method [DirectShow]","IMixerPinConfig interface","dshow.imixerpinconfig_setzorder","mpconfig/IMixerPinConfig::SetZOrder"]
old-location: dshow\imixerpinconfig_setzorder.htm
tech.root: dshow
ms.assetid: fe8e71b8-9aaf-438e-b370-5ba9f131bf7a
ms.date: 12/05/2018
ms.keywords: IMixerPinConfig interface [DirectShow],SetZOrder method, IMixerPinConfig.SetZOrder, IMixerPinConfig::SetZOrder, IMixerPinConfigSetZOrder, SetZOrder, SetZOrder method [DirectShow], SetZOrder method [DirectShow],IMixerPinConfig interface, dshow.imixerpinconfig_setzorder, mpconfig/IMixerPinConfig::SetZOrder
req.header: mpconfig.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMixerPinConfig::SetZOrder
 - mpconfig/IMixerPinConfig::SetZOrder
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IMixerPinConfig.SetZOrder
---

# IMixerPinConfig::SetZOrder


## -description

The <code>SetZOrder</code> method sets the z-order of a particular video stream.



This method is not currently implemented and returns E_NOTIMPL.

## -parameters

### -param dwZOrder [in]

Value indicating the order in which streams will clip each other.

## -returns

Returns E_NOTIMPL.

## -remarks

The z-order indicates which streams can clip other streams. Images with larger z-values are always in front of images with smaller z-values.

The relative order of multiple streams is significant only if the video images overlap.

Specifying the same z-order for two overlapping streams can cause strange video artifacts.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/mpconfig/nn-mpconfig-imixerpinconfig">IMixerPinConfig Interface</a>



<a href="/windows/desktop/api/mpconfig/nf-mpconfig-imixerpinconfig-getzorder">IMixerPinConfig::GetZOrder</a>