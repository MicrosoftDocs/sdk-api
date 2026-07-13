---
UID: NN:tapi3if.ITStream
title: ITStream (tapi3if.h)
description: The ITStream interfaces expose methods that allow an application to retrieve information on a stream; to start, pause, or stop the stream; to select or unselect terminals on a stream; and to obtain a list of terminals selected on the stream.
helpviewer_keywords: ["ITStream","ITStream interface [TAPI 2.2]","ITStream interface [TAPI 2.2]","described","_tapi3_itstream","tapi3.itstream","tapi3if/ITStream"]
old-location: tapi3\itstream.htm
tech.root: tapi3
ms.assetid: 74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a
ms.date: 12/05/2018
ms.keywords: ITStream, ITStream interface [TAPI 2.2], ITStream interface [TAPI 2.2],described, _tapi3_itstream, tapi3.itstream, tapi3if/ITStream
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
 - ITStream
 - tapi3if/ITStream
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
 - ITStream
---

# ITStream interface


## -description

The 
<b>ITStream</b> interfaces expose methods that allow an application to retrieve information on a stream; to start, pause, or stop the stream; to select or unselect terminals on a stream; and to obtain a list of terminals selected on the stream. The following methods create the 
<b>ITStream</b> interface:


<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-createstreamobject">CMSPCallBase::CreateStreamObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumstream-next">IEnumStream::Next</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itsubstream-get_stream">ITSubStream::get_Stream</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-createstream">ITStreamControl::CreateStream</a>

## -inheritance

The <b>ITStream</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITStream</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
