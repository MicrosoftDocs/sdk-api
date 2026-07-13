---
UID: NF:mspstrm.CMSPStream.ShutDown
title: CMSPStream::ShutDown (mspstrm.h)
description: The ShutDown method is called by the MSPCall object. It unselects all the terminal objects (via UnselectTerminal). It also calls MSPCallRelease on the call object. This is needed to break the circular refcount.
helpviewer_keywords: ["CMSPStream interface [TAPI 2.2]","ShutDown method","CMSPStream.ShutDown","CMSPStream::ShutDown","ShutDown","ShutDown method [TAPI 2.2]","ShutDown method [TAPI 2.2]","CMSPStream interface","_tapi3_cmspstream_shutdown","mspstrm/CMSPStream::ShutDown","tapi3.cmspstream_shutdown"]
old-location: tapi3\cmspstream_shutdown.htm
tech.root: tapi3
ms.assetid: 5434c9ea-f045-4293-802d-35fb59123922
ms.date: 12/05/2018
ms.keywords: CMSPStream interface [TAPI 2.2],ShutDown method, CMSPStream.ShutDown, CMSPStream::ShutDown, ShutDown, ShutDown method [TAPI 2.2], ShutDown method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_shutdown, mspstrm/CMSPStream::ShutDown, tapi3.cmspstream_shutdown
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
 - CMSPStream::ShutDown
 - mspstrm/CMSPStream::ShutDown
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
 - CMSPStream.ShutDown
---

# CMSPStream::ShutDown


## -description

The 
<b>ShutDown</b> method is called by the <b>MSPCall</b> object. It unselects all the terminal objects (via 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstream-unselectterminal">UnselectTerminal</a>). It also calls 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-mspcallrelease">MSPCallRelease</a> on the call object. This is needed to break the circular refcount.


