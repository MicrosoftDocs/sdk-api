---
UID: NF:mspcall.CMSPCallMultiGraph.RemoveStream
title: CMSPCallMultiGraph::RemoveStream
author: windows-sdk-content
description: "(Interface RemoveStream) The RemoveStream method is called by the application to remove a stream from the call."
old-location: tapi3\cmspcallmultigraph_removestream.htm
tech.root: Tapi
ms.assetid: 03572d9a-f243-4423-b645-ef180704477f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],RemoveStream method, CMSPCallMultiGraph.RemoveStream, CMSPCallMultiGraph::RemoveStream, RemoveStream, RemoveStream method [TAPI 2.2], RemoveStream method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_removestream, mspcall/CMSPCallMultiGraph::RemoveStream, tapi3.cmspcallmultigraph_removestream
ms.topic: method
req.header: mspcall.h
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
 - Mspcall.h
api_name:
 - CMSPCallMultiGraph.RemoveStream
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPCallMultiGraph::RemoveStream


## -description


(Interface 
<b>RemoveStream</b>) The 
<b>RemoveStream</b> method is called by the application to remove a stream from the call. Derived MSP call objects that do not want to allow applications to remove streams should override this to simply return TAPI_E_NOTSUPPORTED. (This is a good simplification strategy for many MSPs.) The default implementation removes the stream object from the call object's list of streams and releases the call's references to the stream.


## -parameters




### -param ppStream

Pointer to 
<a href="https://msdn.microsoft.com/74a385c8-0c36-4cf0-8983-5ffd7b0e5c4a">ITStream</a> interface for stream to be removed from the call.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms726558(v=VS.85).aspx">CMSPCallMultiGraph</a>
 

 

