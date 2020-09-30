---
UID: NF:d2d1effectauthor.ID2D1DrawTransform.SetDrawInfo
title: ID2D1DrawTransform::SetDrawInfo (d2d1effectauthor.h)
description: Provides the GPU render info interface to the transform implementation.
helpviewer_keywords: ["ID2D1DrawTransform interface [Direct2D]","SetDrawInfo method","ID2D1DrawTransform.SetDrawInfo","ID2D1DrawTransform::SetDrawInfo","SetDrawInfo","SetDrawInfo method [Direct2D]","SetDrawInfo method [Direct2D]","ID2D1DrawTransform interface","d2d1effectauthor/ID2D1DrawTransform::SetDrawInfo","direct2d.id2d1drawtransform_setdrawinfo"]
old-location: direct2d\id2d1drawtransform_setdrawinfo.htm
tech.root: Direct2D
ms.assetid: 9B7336B0-59D8-416F-822C-0AD5C1B40EAA
ms.date: 12/05/2018
ms.keywords: ID2D1DrawTransform interface [Direct2D],SetDrawInfo method, ID2D1DrawTransform.SetDrawInfo, ID2D1DrawTransform::SetDrawInfo, SetDrawInfo, SetDrawInfo method [Direct2D], SetDrawInfo method [Direct2D],ID2D1DrawTransform interface, d2d1effectauthor/ID2D1DrawTransform::SetDrawInfo, direct2d.id2d1drawtransform_setdrawinfo
req.header: d2d1effectauthor.h
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DrawTransform::SetDrawInfo
 - d2d1effectauthor/ID2D1DrawTransform::SetDrawInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1DrawTransform.SetDrawInfo
---

# ID2D1DrawTransform::SetDrawInfo


## -description

    Provides the GPU render info interface to the transform implementation.

## -parameters

### -param drawInfo [in]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo">ID2D1DrawInfo</a>*</b>

The interface supplied back to the calling method to allow it to specify the GPU based transform pass.

## -returns

Type: <b>HRESULT</b>

Any HRESULT value can be returned when implementing this method. A failure will be returned from the corresponding <a href="/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">ID2D1DeviceContext::EndDraw</a> call.

## -remarks

The transform can maintain a  reference to this interface for its lifetime. If any properties change on the transform, it can apply these changes to the corresponding <i>drawInfo</i> interface. 

This is also used to determine that the corresponding nodes in the graph are dirty.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform">ID2D1DrawTransform</a>