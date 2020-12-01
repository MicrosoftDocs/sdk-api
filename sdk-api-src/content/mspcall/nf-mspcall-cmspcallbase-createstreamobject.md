---
UID: NF:mspcall.CMSPCallBase.CreateStreamObject
title: CMSPCallBase::CreateStreamObject (mspcall.h)
description: The CreateStreamObject method is called by InternalCreateStream.
helpviewer_keywords: ["CMSPCallBase interface [TAPI 2.2]","CreateStreamObject method","CMSPCallBase.CreateStreamObject","CMSPCallBase::CreateStreamObject","CreateStreamObject","CreateStreamObject method [TAPI 2.2]","CreateStreamObject method [TAPI 2.2]","CMSPCallBase interface","_tapi3_cmspcallbase_createstreamobject","mspcall/CMSPCallBase::CreateStreamObject","tapi3.cmspcallbase_createstreamobject"]
old-location: tapi3\cmspcallbase_createstreamobject.htm
tech.root: tapi3
ms.assetid: ac98dd08-4250-40f6-91a8-e1f67b94b51f
ms.date: 12/05/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],CreateStreamObject method, CMSPCallBase.CreateStreamObject, CMSPCallBase::CreateStreamObject, CreateStreamObject, CreateStreamObject method [TAPI 2.2], CreateStreamObject method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_createstreamobject, mspcall/CMSPCallBase::CreateStreamObject, tapi3.cmspcallbase_createstreamobject
req.header: mspcall.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPCallBase::CreateStreamObject
 - mspcall/CMSPCallBase::CreateStreamObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.CreateStreamObject
---

# CMSPCallBase::CreateStreamObject


## -description

The 
<b>CreateStreamObject</b> method is called by 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-internalcreatestream">InternalCreateStream</a>. The derived class should <b>CreateInstance</b> on its stream object, do an ATL <b>_InternalQueryInterface</b> to obtain an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> pointer from the stream object, and call the stream object's 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-init">Init</a> method (on the stream object pointer, not the 
<b>ITStream</b> pointer).

## -parameters

### -param dwMediaType

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media type</a> of stream to be created.

### -param Direction

<a href="/windows/desktop/api/tapi3if/ne-tapi3if-terminal_direction">Direction</a> of stream.

### -param pGraph

Pointer to DirectShow <b>IMediaEvent</b> interface.

### -param ppStream

Pointer to 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>