---
UID: NF:ocidl.IViewObjectEx.GetViewStatus
title: IViewObjectEx::GetViewStatus (ocidl.h)
description: Retrieves information about the opacity of the object, and what drawing aspects are supported.
helpviewer_keywords: ["GetViewStatus","GetViewStatus method [COM]","GetViewStatus method [COM]","IViewObjectEx interface","IViewObjectEx interface [COM]","GetViewStatus method","IViewObjectEx.GetViewStatus","IViewObjectEx::GetViewStatus","_ole_iviewobjectex_getviewstatus","com.iviewobjectex_getviewstatus","ocidl/IViewObjectEx::GetViewStatus"]
old-location: com\iviewobjectex_getviewstatus.htm
tech.root: com
ms.assetid: cf8ec90c-07bb-4f60-93c9-4cee3fb5a056
ms.date: 12/05/2018
ms.keywords: GetViewStatus, GetViewStatus method [COM], GetViewStatus method [COM],IViewObjectEx interface, IViewObjectEx interface [COM],GetViewStatus method, IViewObjectEx.GetViewStatus, IViewObjectEx::GetViewStatus, _ole_iviewobjectex_getviewstatus, com.iviewobjectex_getviewstatus, ocidl/IViewObjectEx::GetViewStatus
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IViewObjectEx::GetViewStatus
 - ocidl/IViewObjectEx::GetViewStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IViewObjectEx.GetViewStatus
---

# IViewObjectEx::GetViewStatus


## -description

Retrieves information about the opacity of the object, and what drawing aspects are supported.

## -parameters

### -param pdwStatus [out]

A pointer to the view status. This information is returned as a combination of the <a href="/windows/desktop/api/ocidl/ne-ocidl-viewstatus">VIEWSTATUS</a> enumeration values.

## -returns

This method returns S_OK on success.

## -remarks

In order to optimize the drawing process, the container needs to be able to determine whether an object is opaque and whether it has a solid background. It is not necessary to redraw objects that are entirely covered by a completely opaque object. Other operations, such as scrolling for example, can also be highly optimized if an object is opaque and has a solid background.

The <b>IViewObjectEx::GetViewStatus</b> method returns whether the object is entirely opaque or not (VIEWSTATUS_OPAQUE bit) and whether its background is solid (VIEWSTATUS_SOLIDBKGND bit). This information may change in time. An object may be opaque at a given time and become totally or partially transparent later on, for example, because of a change of the BackStyle property. An object should notify its sites when it changes using <a href="/windows/desktop/api/ocidl/nf-ocidl-iadvisesinkex-onviewstatuschange">IAdviseSinkEx::OnViewStatusChange</a> so the sites can cache this information for high speed access.

Objects not supporting <a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a> are considered to be always transparent.

The <b>IViewObjectEx::GetViewStatus</b> method also returns a combination of bits indicating which aspects are supported.

If a given drawing aspect is not supported, all <a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a> methods taking a drawing aspect as an input parameter should fail and return E_INVALIDARG. The <b>IViewObjectEx::GetViewStatus</b> method allows the container to get back information about all drawing aspects in one quick call. Normally the set of supported drawing aspects should not change with time. However, if this was not the case, an object should notify its container using <a href="/windows/desktop/api/ocidl/nf-ocidl-iadvisesinkex-onviewstatuschange">IAdviseSinkEx::OnViewStatusChange</a>.

Which drawing aspects are supported is independent of whether the object is opaque, partially transparent, or totally transparent. In particular, a transparent object that does not support DVASPECT_TRANSPARENT should be drawn correctly during the back to front pass using DVASPECT_CONTENT. However, this is likely to result in more flicker.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iadvisesinkex-onviewstatuschange">IAdviseSinkEx::OnViewStatusChange</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iviewobjectex">IViewObjectEx</a>



<a href="/windows/desktop/api/ocidl/ne-ocidl-viewstatus">VIEWSTATUS</a>