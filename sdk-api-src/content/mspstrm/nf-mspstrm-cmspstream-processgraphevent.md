---
UID: NF:mspstrm.CMSPStream.ProcessGraphEvent
title: CMSPStream::ProcessGraphEvent (mspstrm.h)
author: windows-sdk-content
description: The ProcessGraphEvent method is called by the MSPCall object to let the stream handle graph events.
old-location: tapi3\cmspstream_processgraphevent.htm
tech.root: Tapi
ms.assetid: 343411de-956d-4264-8bab-ce0c2459f6d1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CMSPStream interface [TAPI 2.2],ProcessGraphEvent method, CMSPStream.ProcessGraphEvent, CMSPStream::ProcessGraphEvent, ProcessGraphEvent, ProcessGraphEvent method [TAPI 2.2], ProcessGraphEvent method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_processgraphevent, mspstrm/CMSPStream::ProcessGraphEvent, tapi3.cmspstream_processgraphevent
ms.topic: method
f1_keywords: 
 - "mspstrm/CMSPStream.ProcessGraphEvent"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspstrm.h
api_name:
 - CMSPStream.ProcessGraphEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/mspstrm/nl-mspstrm-cmspstream">CMSPStream</a>
 

 

