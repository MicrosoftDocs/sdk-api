---
UID: NF:ocidl.IQuickActivate.QuickActivate
title: IQuickActivate::QuickActivate (ocidl.h)
description: Quick activates a control.
helpviewer_keywords: ["IQuickActivate interface [COM]","QuickActivate method","IQuickActivate.QuickActivate","IQuickActivate::QuickActivate","QuickActivate","QuickActivate method [COM]","QuickActivate method [COM]","IQuickActivate interface","_ctrl_iquickactivate_quickactivate","com.iquickactivate_quickactivate","ocidl/IQuickActivate::QuickActivate"]
old-location: com\iquickactivate_quickactivate.htm
tech.root: com
ms.assetid: 504cb272-da1c-4ffb-b4b1-fdf288901660
ms.date: 12/05/2018
ms.keywords: IQuickActivate interface [COM],QuickActivate method, IQuickActivate.QuickActivate, IQuickActivate::QuickActivate, QuickActivate, QuickActivate method [COM], QuickActivate method [COM],IQuickActivate interface, _ctrl_iquickactivate_quickactivate, com.iquickactivate_quickactivate, ocidl/IQuickActivate::QuickActivate
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - IQuickActivate::QuickActivate
 - ocidl/IQuickActivate::QuickActivate
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
 - IQuickActivate.QuickActivate
---

# IQuickActivate::QuickActivate


## -description

Quick activates a control.

## -parameters

### -param pQaContainer [in]

A pointer to the <a href="/windows/desktop/api/ocidl/ns-ocidl-qacontainer">QACONTAINER</a> structure containing information about the container.

### -param pQaControl [in, out]

A pointer to the <a href="/windows/desktop/api/ocidl/ns-ocidl-qacontrol">QACONTROL</a> structure filled in by the control to return information about the control to the container. The container calling this method must reserve memory for this structure.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -remarks

If the control does not support <a href="/windows/desktop/api/ocidl/nn-ocidl-iquickactivate">IQuickActivate</a>, the container performs certain handshaking operations when it loads the control. The container calls certain interfaces on the control and the control, in turn, calls back to certain interfaces on the container's client site. First, the container creates the control object and calls <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to query for interfaces that it needs. Then, the container calls <a href="/windows/desktop/api/oleidl/nf-oleidl-ioleobject-setclientsite">IOleObject::SetClientSite</a> on the control, passing a pointer to its client site. Next, the control calls <b>QueryInterface</b> on this site, retrieving a pointer to additional necessary interfaces.

Using the <b>QuickActivate</b> method, the container passes a pointer to a <a href="/windows/desktop/api/ocidl/ns-ocidl-qacontainer">QACONTAINER</a> structure. The structure contains pointers to interfaces which are needed by the control and the values of some ambient properties that the control may need. Upon return, the control passes a pointer to a <a href="/windows/desktop/api/ocidl/ns-ocidl-qacontrol">QACONTROL</a> structure that contains pointers to its own interfaces that the container requires, and additional status information.

The <b>IPersist*::Load</b> and <b>IPersist*::InitNew</b> methods should be called after quick activation occurs. The control should establish its connections to the container's sinks during quick activation. However, these connections are not live until <b>IPersist*::Load</b> or <b>IPersist*::InitNew</b> has been called.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-ipersistfile">IPersistFile</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>



<a href="/windows/desktop/api/objidl/nn-objidl-ipersiststream">IPersistStream</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-ipersiststreaminit">IPersistStreamInit</a>



<a href="/windows/desktop/api/ocidl/nn-ocidl-iquickactivate">IQuickActivate</a>