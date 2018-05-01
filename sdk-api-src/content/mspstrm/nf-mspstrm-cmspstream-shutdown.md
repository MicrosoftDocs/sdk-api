---
UID: NF:mspstrm.CMSPStream.ShutDown
title: CMSPStream::ShutDown method
author: windows-driver-content
description: The ShutDown method is called by the MSPCall object. It unselects all the terminal objects (via UnselectTerminal). It also calls MSPCallRelease on the call object. This is needed to break the circular refcount.
old-location: tapi3\cmspstream_shutdown.htm
old-project: Tapi
ms.assetid: 5434c9ea-f045-4293-802d-35fb59123922
ms.author: windowsdriverdev
ms.date: 4/16/2018
ms.keywords: CMSPStream, CMSPStream interface [TAPI 2.2], ShutDown method, CMSPStream::ShutDown, ShutDown method [TAPI 2.2], ShutDown method [TAPI 2.2], CMSPStream interface, ShutDown,CMSPStream.ShutDown, _tapi3_cmspstream_shutdown, mspstrm/CMSPStream::ShutDown, tapi3.cmspstream_shutdown
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
-	CMSPStream.ShutDown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CMSPStream::ShutDown method


## -description


The 
<b>ShutDown</b> method is called by the <b>MSPCall</b> object. It unselects all the terminal objects (via 
<a href="https://msdn.microsoft.com/ad16ea41-0c02-4bba-bfd9-267b56c481e1">UnselectTerminal</a>). It also calls 
<a href="https://msdn.microsoft.com/662361f2-ce0c-4c07-88c1-30393a236bf6">MSPCallRelease</a> on the call object. This is needed to break the circular refcount.


## -parameters





