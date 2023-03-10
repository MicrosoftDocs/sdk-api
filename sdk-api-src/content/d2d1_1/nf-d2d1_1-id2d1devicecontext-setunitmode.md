---
UID: NF:d2d1_1.ID2D1DeviceContext.SetUnitMode
title: ID2D1DeviceContext::SetUnitMode (d2d1_1.h)
description: Sets what units will be used to interpret values passed into the device context.
helpviewer_keywords: ["ID2D1DeviceContext interface [Direct2D]","SetUnitMode method","ID2D1DeviceContext.SetUnitMode","ID2D1DeviceContext::SetUnitMode","SetUnitMode","SetUnitMode method [Direct2D]","SetUnitMode method [Direct2D]","ID2D1DeviceContext interface","d2d1_1/ID2D1DeviceContext::SetUnitMode","direct2d.id2d1devicecontext_setunitmode"]
old-location: direct2d\id2d1devicecontext_setunitmode.htm
tech.root: Direct2D
ms.assetid: a5774b9a-4458-47e7-821a-4ac4b70468e3
ms.date: 12/05/2018
ms.keywords: ID2D1DeviceContext interface [Direct2D],SetUnitMode method, ID2D1DeviceContext.SetUnitMode, ID2D1DeviceContext::SetUnitMode, SetUnitMode, SetUnitMode method [Direct2D], SetUnitMode method [Direct2D],ID2D1DeviceContext interface, d2d1_1/ID2D1DeviceContext::SetUnitMode, direct2d.id2d1devicecontext_setunitmode
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
req.lib: 
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DeviceContext::SetUnitMode
 - d2d1_1/ID2D1DeviceContext::SetUnitMode
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
 - ID2D1DeviceContext.SetUnitMode
---

# ID2D1DeviceContext::SetUnitMode


## -description

Sets what units will be used to interpret values passed into the device context.

## -parameters

### -param unitMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_unit_mode">D2D1_UNIT_MODE</a></b>

An enumeration defining how passed-in units will be interpreted by the device context.

## -remarks

This method will affect all properties and parameters affected by <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-setdpi">SetDpi</a> 
        and <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-getdpi">GetDpi</a>. This affects all coordinates, lengths, and other properties that are 
        not explicitly defined as being in another unit. For example:

<ul>
<li><b>SetUnitMode</b> will affect a coordinate passed 
            into <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawline">ID2D1DeviceContext::DrawLine</a>, and the scaling of a 
            geometry passed into <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry">ID2D1DeviceContext::FillGeometry</a>.
          </li>
<li><b>SetUnitMode</b> will not affect the value
            returned by <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1bitmap-getpixelsize">ID2D1Bitmap::GetPixelSize</a>.
          </li>
</ul>

## -see-also

<a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_unit_mode">D2D1_UNIT_MODE</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>