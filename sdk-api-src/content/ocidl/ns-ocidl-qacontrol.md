---
UID: NS:ocidl.tagQACONTROL
title: QACONTROL (ocidl.h)
description: Specifies control information for IQuickActivate::QuickActivate.
helpviewer_keywords: ["QACONTROL","QACONTROL structure [COM]","_ctrl_QACONTROL","com.qacontrol","ocidl/QACONTROL"]
old-location: com\qacontrol.htm
tech.root: com
ms.assetid: dd7ee4b1-2ad9-4ceb-b569-9988696760e8
ms.date: 12/05/2018
ms.keywords: QACONTROL, QACONTROL structure [COM], _ctrl_QACONTROL, com.qacontrol, ocidl/QACONTROL
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
req.typenames: QACONTROL
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagQACONTROL
 - ocidl/tagQACONTROL
 - QACONTROL
 - ocidl/QACONTROL
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - OCIdl.h
api_name:
 - QACONTROL
---

# QACONTROL structure


## -description

Specifies control information for  <a href="/windows/desktop/api/ocidl/nf-ocidl-iquickactivate-quickactivate">IQuickActivate::QuickActivate</a>.

## -struct-fields

### -field cbSize

The size of the structure, in bytes.

### -field dwMiscStatus

The control's miscellaneous status bits that can also be returned by <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-getmiscstatus">IOleObject::GetMiscStatus</a>. See <a href="/windows/desktop/api/oleidl/ne-oleidl-olemisc">OLEMISC</a> for more information.

### -field dwViewStatus

The control's view status that can also be returned by <a href="/windows/desktop/api/ocidl/nf-ocidl-iviewobjectex-getviewstatus">IViewObjectEx::GetViewStatus</a>. See <a href="/windows/desktop/api/ocidl/ne-ocidl-viewstatus">VIEWSTATUS</a> for more information.

### -field dwEventCookie

A unique identifier for control-defined events.

### -field dwPropNotifyCookie

A unique identifier for control-defined properties.

### -field dwPointerActivationPolicy

The control's activation policy that can also be returned by <a href="/windows/desktop/api/ocidl/nf-ocidl-ipointerinactive-getactivationpolicy">IPointerInactive::GetActivationPolicy</a>. If all the bits of <b>dwPointerActivationPolicy</b> are set, then the IPointerInactive interface may not be supported. The container should <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to obtain the interface pointer in the standard manner.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iquickactivate-quickactivate">IQuickActivate::QuickActivate</a>