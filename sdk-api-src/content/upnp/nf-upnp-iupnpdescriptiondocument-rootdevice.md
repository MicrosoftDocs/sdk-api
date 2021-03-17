---
UID: NF:upnp.IUPnPDescriptionDocument.RootDevice
title: IUPnPDescriptionDocument::RootDevice (upnp.h)
description: The RootDevice method returns the root device of the currently loaded document's device tree.
helpviewer_keywords: ["IUPnPDescriptionDocument interface [UPnP APIs]","RootDevice method","IUPnPDescriptionDocument.RootDevice","IUPnPDescriptionDocument::RootDevice","RootDevice","RootDevice method [UPnP APIs]","RootDevice method [UPnP APIs]","IUPnPDescriptionDocument interface","_upnp_iupnpdescriptiondocument_rootdevice","upnp.iupnpdescriptiondocument_rootdevice","upnp/IUPnPDescriptionDocument::RootDevice"]
old-location: upnp\iupnpdescriptiondocument_rootdevice.htm
tech.root: upnp
ms.assetid: 0caa4f1e-0c74-4654-be26-6178aefa3ee4
ms.date: 12/05/2018
ms.keywords: IUPnPDescriptionDocument interface [UPnP APIs],RootDevice method, IUPnPDescriptionDocument.RootDevice, IUPnPDescriptionDocument::RootDevice, RootDevice, RootDevice method [UPnP APIs], RootDevice method [UPnP APIs],IUPnPDescriptionDocument interface, _upnp_iupnpdescriptiondocument_rootdevice, upnp.iupnpdescriptiondocument_rootdevice, upnp/IUPnPDescriptionDocument::RootDevice
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Upnp.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUPnPDescriptionDocument::RootDevice
 - upnp/IUPnPDescriptionDocument::RootDevice
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPDescriptionDocument.RootDevice
---

# IUPnPDescriptionDocument::RootDevice


## -description

The 
<b>RootDevice</b> method returns the root device of the currently loaded document's device tree.

## -parameters

### -param ppudRootDevice [out]

Receives a reference to an 
<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a> object that describes the device. This reference must be released when it is no longer required.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, the method returns one of the COM error codes defined in WinError.h.

## -remarks

Do not use 
<b>RootDevice</b> unless a device description is first loaded using either 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-load">IUPnPDescriptionDocument::Load</a> or 
<a href="/windows/desktop/api/upnp/nf-upnp-iupnpdescriptiondocument-loadasync">IUPnPDescriptionDocument::LoadAsync</a>. The search operation only searches in the currently loaded device description.

## -see-also

<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdescriptiondocument">IUPnPDescriptionDocument</a>



<a href="/windows/desktop/api/upnp/nn-upnp-iupnpdevice">IUPnPDevice</a>