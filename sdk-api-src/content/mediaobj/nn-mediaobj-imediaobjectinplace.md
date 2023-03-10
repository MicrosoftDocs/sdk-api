---
UID: NN:mediaobj.IMediaObjectInPlace
title: IMediaObjectInPlace (mediaobj.h)
description: The IMediaObjectInPlace interface provides methods for processing data in place. A Microsoft DirectX Media Object (DMO) can expose this interface if it meets the following conditions:\_
helpviewer_keywords: ["IMediaObjectInPlace","IMediaObjectInPlace interface [DirectShow]","IMediaObjectInPlace interface [DirectShow]","described","IMediaObjectInPlaceInterface","dshow.imediaobjectinplace","mediaobj/IMediaObjectInPlace"]
old-location: dshow\imediaobjectinplace.htm
tech.root: dshow
ms.assetid: c2105141-6c5e-4edb-aa3b-3227ca223329
ms.date: 12/05/2018
ms.keywords: IMediaObjectInPlace, IMediaObjectInPlace interface [DirectShow], IMediaObjectInPlace interface [DirectShow],described, IMediaObjectInPlaceInterface, dshow.imediaobjectinplace, mediaobj/IMediaObjectInPlace
req.header: mediaobj.h
req.include-header: Dmo.h
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
req.lib: Dmoguids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMediaObjectInPlace
 - mediaobj/IMediaObjectInPlace
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dmoguids.lib
 - Dmoguids.dll
api_name:
 - IMediaObjectInPlace
---

# IMediaObjectInPlace interface


## -description

The <code>IMediaObjectInPlace</code> interface provides methods for processing data in place. A Microsoft DirectX Media Object (DMO) can expose this interface if it meets the following conditions:


<ul>
<li>It has one input stream and one output stream.</li>
<li>Both streams use the same media type.</li>
<li>The output is produced in place on the buffer; that is, without copying data.</li>
</ul>This interface provides an optimized way to process data. The application calls a single <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobjectinplace-process">IMediaObjectInPlace::Process</a> method instead of the <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processinput">IMediaObject::ProcessInput</a> and <a href="/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput">IMediaObject::ProcessOutput</a> methods. However, any DMO that implements this interface must also implement the <a href="/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject">IMediaObject</a> interface. Therefore, an application is never obligated to use this interface, and a DMO is never guaranteed to implement it.

## -inheritance

The <b>IMediaObjectInPlace</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMediaObjectInPlace</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

