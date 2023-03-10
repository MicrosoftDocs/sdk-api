---
UID: NN:tapi3if.ITSubStream
title: ITSubStream (tapi3if.h)
description: An ITSubStream is a component of an ITStream, and gives an application finer control over the media streaming.
helpviewer_keywords: ["ITSubStream","ITSubStream interface [TAPI 2.2]","ITSubStream interface [TAPI 2.2]","described","_tapi3_itsubstream","tapi3.itsubstream","tapi3if/ITSubStream"]
old-location: tapi3\itsubstream.htm
tech.root: tapi3
ms.assetid: fc495bc3-1172-4e39-b617-055b7ac95898
ms.date: 12/05/2018
ms.keywords: ITSubStream, ITSubStream interface [TAPI 2.2], ITSubStream interface [TAPI 2.2],described, _tapi3_itsubstream, tapi3.itsubstream, tapi3if/ITSubStream
req.header: tapi3if.h
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
 - ITSubStream
 - tapi3if/ITSubStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3if.h
api_name:
 - ITSubStream
---

# ITSubStream interface


## -description

An 
<b>ITSubStream</b> is a component of an 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>, and gives an application finer control over the media streaming. The 
<b>ITSubStream</b> interface provides methods that start, pause, or stop a substream, select or unselect terminals, and obtain a list of terminals selected on the stream. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumsubstream-next">IEnumSubStream::Next</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstreamcontrol-createsubstream">ITSubStreamControl::CreateSubStream</a> methods create the 
<b>ITSubStream</b> interface.

## -inheritance

The <b>ITSubStream</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITSubStream</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
