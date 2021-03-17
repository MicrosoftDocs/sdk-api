---
UID: NF:d2d1_1.ID2D1CommandSink.SetUnitMode
title: ID2D1CommandSink::SetUnitMode (d2d1_1.h)
description: The unit mode changes the meaning of subsequent units from device-independent pixels (DIPs) to pixels or the other way. The command sink does not record a DPI, this is implied by the playback context or other playback interface such as ID2D1PrintControl.
helpviewer_keywords: ["ID2D1CommandSink interface [Direct2D]","SetUnitMode method","ID2D1CommandSink.SetUnitMode","ID2D1CommandSink::SetUnitMode","SetUnitMode","SetUnitMode method [Direct2D]","SetUnitMode method [Direct2D]","ID2D1CommandSink interface","d2d1_1/ID2D1CommandSink::SetUnitMode","direct2d.id2d1commandsink_setunitmode"]
old-location: direct2d\id2d1commandsink_setunitmode.htm
tech.root: Direct2D
ms.assetid: e524aa51-2499-4333-9562-a4893666b666
ms.date: 12/05/2018
ms.keywords: ID2D1CommandSink interface [Direct2D],SetUnitMode method, ID2D1CommandSink.SetUnitMode, ID2D1CommandSink::SetUnitMode, SetUnitMode, SetUnitMode method [Direct2D], SetUnitMode method [Direct2D],ID2D1CommandSink interface, d2d1_1/ID2D1CommandSink::SetUnitMode, direct2d.id2d1commandsink_setunitmode
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
 - ID2D1CommandSink::SetUnitMode
 - d2d1_1/ID2D1CommandSink::SetUnitMode
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
 - ID2D1CommandSink.SetUnitMode
---

# ID2D1CommandSink::SetUnitMode


## -description

The unit mode changes the meaning of subsequent units from device-independent pixels (DIPs) to pixels  or the other way. The command sink does not record a DPI, this is implied by the playback context or other playback interface such as <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1printcontrol">ID2D1PrintControl</a>.

## -parameters

### -param unitMode

Type: <b><a href="/windows/desktop/api/d2d1_1/ne-d2d1_1-d2d1_unit_mode">D2D1_UNIT_MODE</a></b>

The enumeration that specifies how units are to be interpreted.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The unit mode changes the interpretation of units from DIPs to pixels  or vice versa.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandlist-stream">ID2D1CommandList::Stream</a>



<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandsink">ID2D1CommandSink</a>



<a href="/windows/desktop/Direct2D/id2d1rendertarget-settransform">ID2D1RenderTarget::SetTransform</a>