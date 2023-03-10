---
UID: NF:mspstrm.CMSPStream.GetState
title: CMSPStream::GetState (mspstrm.h)
description: The GetState method is called by the MSPCall object. It returns the current status of the stream. The default implementation returns E_NOTIMPL.
helpviewer_keywords: ["CMSPStream interface [TAPI 2.2]","GetState method","CMSPStream.GetState","CMSPStream::GetState","GetState","GetState method [TAPI 2.2]","GetState method [TAPI 2.2]","CMSPStream interface","_tapi3_cmspstream_getstate","mspstrm/CMSPStream::GetState","tapi3.cmspstream_getstate"]
old-location: tapi3\cmspstream_getstate.htm
tech.root: tapi3
ms.assetid: 03fc3801-8bd4-432a-b0ca-f6506bd8c788
ms.date: 12/05/2018
ms.keywords: CMSPStream interface [TAPI 2.2],GetState method, CMSPStream.GetState, CMSPStream::GetState, GetState, GetState method [TAPI 2.2], GetState method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_getstate, mspstrm/CMSPStream::GetState, tapi3.cmspstream_getstate
req.header: mspstrm.h
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
 - CMSPStream::GetState
 - mspstrm/CMSPStream::GetState
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspstrm.h
api_name:
 - CMSPStream.GetState
---

# CMSPStream::GetState


## -description

The 
<b>GetState</b> method is called by the MSPCall object. It returns the current status of the stream. The default implementation returns E_NOTIMPL.

## -parameters

### -param pdwStatus

Pointer to indication of stream's state. The precise return value is implementation dependent. An example set of types that might be defined for this purpose: STRM_RUNNING, STRM_PAUSED, and STRM_STOPPED.

## -see-also

<a href="/windows/desktop/api/mspstrm/nl-mspstrm-cmspstream">CMSPStream</a>