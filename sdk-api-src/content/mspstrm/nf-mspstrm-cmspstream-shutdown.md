---
UID: NF:mspstrm.CMSPStream.ShutDown
title: CMSPStream::ShutDown (mspstrm.h)
author: windows-sdk-content
description: The ShutDown method is called by the MSPCall object. It unselects all the terminal objects (via UnselectTerminal). It also calls MSPCallRelease on the call object. This is needed to break the circular refcount.
old-location: tapi3\cmspstream_shutdown.htm
tech.root: Tapi
ms.assetid: 5434c9ea-f045-4293-802d-35fb59123922
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CMSPStream interface [TAPI 2.2],ShutDown method, CMSPStream.ShutDown, CMSPStream::ShutDown, ShutDown, ShutDown method [TAPI 2.2], ShutDown method [TAPI 2.2],CMSPStream interface, _tapi3_cmspstream_shutdown, mspstrm/CMSPStream::ShutDown, tapi3.cmspstream_shutdown
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
 - CMSPStream.ShutDown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPStream::ShutDown


## -description


The 
<b>ShutDown</b> method is called by the <b>MSPCall</b> object. It unselects all the terminal objects (via 
<a href="https://msdn.microsoft.com/ad16ea41-0c02-4bba-bfd9-267b56c481e1">UnselectTerminal</a>). It also calls 
<a href="https://msdn.microsoft.com/en-us/library/ms726528(v=VS.85).aspx">MSPCallRelease</a> on the call object. This is needed to break the circular refcount.


## -parameters





