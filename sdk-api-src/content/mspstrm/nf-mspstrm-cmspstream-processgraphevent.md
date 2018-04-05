---
UID: NF:mspstrm.CMSPStream.ProcessGraphEvent
title: CMSPStream::ProcessGraphEvent method
author: windows-driver-content
description: The ProcessGraphEvent method is called by the MSPCall object to let the stream handle graph events.
old-location: tapi3\cmspstream_processgraphevent.htm
old-project: Tapi
ms.assetid: 343411de-956d-4264-8bab-ce0c2459f6d1
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CMSPStream, CMSPStream interface [TAPI 2.2], ProcessGraphEvent method, CMSPStream::ProcessGraphEvent, ProcessGraphEvent method [TAPI 2.2], ProcessGraphEvent method [TAPI 2.2], CMSPStream interface, ProcessGraphEvent,CMSPStream.ProcessGraphEvent, _tapi3_cmspstream_processgraphevent, mspstrm/CMSPStream::ProcessGraphEvent, tapi3.cmspstream_processgraphevent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Mspstrm.h
api_name:
-	CMSPStream.ProcessGraphEvent
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CMSPStream::ProcessGraphEvent method


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




<a href="https://msdn.microsoft.com/776ca663-faa2-4534-8873-4e20ed79530c">CMSPStream</a>
 

 

