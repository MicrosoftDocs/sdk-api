---
UID: NF:mspstrm.CMSPStream.ProcessGraphEvent
title: CMSPStream::ProcessGraphEvent (mspstrm.h)
description: The ProcessGraphEvent method is called by the MSPCall object to let the stream handle graph events.
helpviewer_keywords: ["CMSPStream interface [TAPI 2.2]","ProcessGraphEvent method","CMSPStream.ProcessGraphEvent","CMSPStream::ProcessGraphEvent","ProcessGraphEvent","ProcessGraphEvent method [TAPI 2.2]","ProcessGraphEvent method [TAPI 2.2]","CMSPStream interface","_tapi3_cmspstream_processgraphevent","mspstrm/CMSPStream::ProcessGraphEvent","tapi3.cmspstream_processgraphevent"]
old-location: tapi3\cmspstream_processgraphevent.htm
tech.root: tapi3
ms.assetid: 343411de-956d-4264-8bab-ce0c2459f6d1
ms.date: 12/05/2018
ms.keywords: CMSPStream interface [TAPI 2.2],ProcessGraphEvent method, CMSPStream.ProcessGraphEvent, CMSPStream::ProcessGraphEvent, ProcessGraphEvent, ProcessGraphEvent method [TAPI 2.2], ProcessGraphEvent method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_processgraphevent, mspstrm/CMSPStream::ProcessGraphEvent, tapi3.cmspstream_processgraphevent
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
 - CMSPStream::ProcessGraphEvent
 - mspstrm/CMSPStream::ProcessGraphEvent
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
 - CMSPStream.ProcessGraphEvent
---

# CMSPStream::ProcessGraphEvent


## -description

The 
<b>ProcessGraphEvent</b> method is called by the MSPCall object to let the stream handle graph events. The default implementation returns S_OK and does nothing. Derived MSPs must override this method if they want to propagate graph events to the application or take some other action in response to graph events.

## -parameters

### -param lEventCode

Implementation-dependent descriptor of the graph event.

### -param lParam1

Implementation-dependent information on the graph event.

### -param lParam2

Implementation-dependent information on the graph event.

## -see-also

<a href="/windows/desktop/api/mspstrm/nl-mspstrm-cmspstream">CMSPStream</a>