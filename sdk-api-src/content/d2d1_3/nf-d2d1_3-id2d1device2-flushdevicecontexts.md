---
UID: NF:d2d1_3.ID2D1Device2.FlushDeviceContexts
title: ID2D1Device2::FlushDeviceContexts (d2d1_3.h)
description: Flush all device contexts that reference a given bitmap.
helpviewer_keywords: ["FlushDeviceContexts","FlushDeviceContexts method [Direct2D]","FlushDeviceContexts method [Direct2D]","ID2D1Device2 interface","ID2D1Device2 interface [Direct2D]","FlushDeviceContexts method","ID2D1Device2.FlushDeviceContexts","ID2D1Device2::FlushDeviceContexts","d2d1_3/ID2D1Device2::FlushDeviceContexts","direct2d.id2d1device2_flushdevicecontexts"]
old-location: direct2d\id2d1device2_flushdevicecontexts.htm
tech.root: Direct2D
ms.assetid: 914A64BA-61CD-4A66-91D8-F7CC040AF67A
ms.date: 12/05/2018
ms.keywords: FlushDeviceContexts, FlushDeviceContexts method [Direct2D], FlushDeviceContexts method [Direct2D],ID2D1Device2 interface, ID2D1Device2 interface [Direct2D],FlushDeviceContexts method, ID2D1Device2.FlushDeviceContexts, ID2D1Device2::FlushDeviceContexts, d2d1_3/ID2D1Device2::FlushDeviceContexts, direct2d.id2d1device2_flushdevicecontexts
req.header: d2d1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1_3.lib
req.dll: D2d1_3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Device2::FlushDeviceContexts
 - d2d1_3/ID2D1Device2::FlushDeviceContexts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1_3.dll
api_name:
 - ID2D1Device2.FlushDeviceContexts
---

# ID2D1Device2::FlushDeviceContexts


## -description

Flush all device contexts that reference a given bitmap.

## -parameters

### -param bitmap [in]

Type: <b><a href="/windows/desktop/api/d2d1/nn-d2d1-id2d1bitmap">ID2D1Bitmap</a>*</b>

The bitmap, created on this device, for which all referencing device contexts will be flushed.

## -see-also

<a href="/windows/desktop/api/d2d1_3/nn-d2d1_3-id2d1device2">ID2D1Device2</a>