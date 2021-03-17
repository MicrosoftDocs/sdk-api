---
UID: NS:ocidl.tagQACONTAINER
title: QACONTAINER (ocidl.h)
description: Specifies container information for IQuickActivate::QuickActivate.
helpviewer_keywords: ["QACONTAINER","QACONTAINER structure [COM]","_ctrl_QACONTAINER","com.qacontainer","ocidl/QACONTAINER"]
old-location: com\qacontainer.htm
tech.root: com
ms.assetid: 8f3975eb-7cd2-449f-92cc-2b8773d9f37e
ms.date: 12/05/2018
ms.keywords: QACONTAINER, QACONTAINER structure [COM], _ctrl_QACONTAINER, com.qacontainer, ocidl/QACONTAINER
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
req.typenames: QACONTAINER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagQACONTAINER
 - ocidl/tagQACONTAINER
 - QACONTAINER
 - ocidl/QACONTAINER
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
 - QACONTAINER
---

# QACONTAINER structure


## -description

Specifies container information for <a href="/windows/desktop/api/ocidl/nf-ocidl-iquickactivate-quickactivate">IQuickActivate::QuickActivate</a>.

## -struct-fields

### -field cbSize

The size of the structure, in bytes.

### -field pClientSite

A pointer to an <a href="/windows/desktop/api/oleidl/nn-oleidl-ioleclientsite">IOleClientSite</a> interface in the container.

### -field pAdviseSink

A pointer to an <a href="/windows/desktop/api/ocidl/nn-ocidl-iadvisesinkex">IAdviseSinkEx</a> interface in the container.

### -field pPropertyNotifySink

A pointer to an <a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertynotifysink">IPropertyNotifySink</a> interface in the container.

### -field pUnkEventSink

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface on the container's sink object.

### -field dwAmbientFlags

The number of ambient properties supplied by the container using values from the <a href="/windows/desktop/api/ocidl/ne-ocidl-qacontainerflags">QACONTAINERFLAGS</a> enumeration.

### -field colorFore

Specifies ForeColor, an ambient property supplied by the container with a DISPID = -704.

### -field colorBack

Specifies BackColor, an ambient property supplied by the container with a DISPID = -701.

### -field pFont

Specifies Font, an ambient property supplied by the container with a DISPID = -703.

### -field pUndoMgr

A pointer to an <a href="/windows/desktop/api/ocidl/nn-ocidl-ioleundomanager">IOleUndoManager</a> interface in the container.

### -field dwAppearance

Specifies Appearance, an ambient property supplied by the container with a DISPID = -716.

### -field lcid

Specifies LocaleIdentifier, an ambient property supplied by the container with a DISPID = -705.

### -field hpal

Specifies Palette, an ambient property supplied by the container with a DISPID = -726.

### -field pBindHost

A pointer to an <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)">IBindHost</a> interface in the container.

### -field pOleControlSite

A pointer to the <a href="/windows/desktop/api/ocidl/nn-ocidl-iolecontrolsite">IOleControlSite</a> interface in the container's site object.

### -field pServiceProvider

A pointer to the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)">IServiceProvider</a> interface in the container.

## -remarks

If an interface pointer in the <b>QACONTAINER</b> structure is <b>NULL</b> it does not indicate that the interface is not supported. In this situation, the control should use <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to obtain the interface pointer in the standard manner.

## -see-also

<a href="/windows/desktop/api/ocidl/nf-ocidl-iquickactivate-quickactivate">IQuickActivate::QuickActivate</a>



<a href="/windows/desktop/api/ocidl/ne-ocidl-qacontainerflags">QACONTAINERFLAGS</a>