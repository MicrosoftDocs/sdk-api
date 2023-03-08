---
UID: NF:d2d1_1.ID2D1Device.SetMaximumTextureMemory
title: ID2D1Device::SetMaximumTextureMemory (d2d1_1.h)
description: Sets the maximum amount of texture memory Direct2D accumulates before it purges the image caches and cached texture allocations. (ID2D1Device.SetMaximumTextureMemory)
helpviewer_keywords: ["ID2D1Device interface [Direct2D]","SetMaximumTextureMemory method","ID2D1Device.SetMaximumTextureMemory","ID2D1Device::SetMaximumTextureMemory","SetMaximumTextureMemory","SetMaximumTextureMemory method [Direct2D]","SetMaximumTextureMemory method [Direct2D]","ID2D1Device interface","d2d1_1/ID2D1Device::SetMaximumTextureMemory","direct2d.id2d1device_setmaximumtexturememory"]
old-location: direct2d\id2d1device_setmaximumtexturememory.htm
tech.root: Direct2D
ms.assetid: 8B714995-8837-4605-8CA3-7D7941D2C10D
ms.date: 12/05/2018
ms.keywords: ID2D1Device interface [Direct2D],SetMaximumTextureMemory method, ID2D1Device.SetMaximumTextureMemory, ID2D1Device::SetMaximumTextureMemory, SetMaximumTextureMemory, SetMaximumTextureMemory method [Direct2D], SetMaximumTextureMemory method [Direct2D],ID2D1Device interface, d2d1_1/ID2D1Device::SetMaximumTextureMemory, direct2d.id2d1device_setmaximumtexturememory
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1Device::SetMaximumTextureMemory
 - d2d1_1/ID2D1Device::SetMaximumTextureMemory
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1Device.SetMaximumTextureMemory
---

# ID2D1Device::SetMaximumTextureMemory


## -description

Sets the maximum amount of texture memory Direct2D accumulates before it purges the image caches and cached texture allocations.

## -parameters

### -param maximumInBytes

Type: <b>UINT64</b>

The new maximum texture memory in bytes.

## -remarks

<div class="alert"><b>Note</b>  Direct2D may exceed the  maximum texture memory you set with this method for a single frame if necessary to render the frame.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1device">ID2D1Device</a>
