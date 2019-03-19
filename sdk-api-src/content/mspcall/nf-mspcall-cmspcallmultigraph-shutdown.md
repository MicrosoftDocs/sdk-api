---
UID: NF:mspcall.CMSPCallMultiGraph.ShutDown
title: CMSPCallMultiGraph::ShutDown (mspcall.h)
author: windows-sdk-content
description: The ShutDown method is called by the MSP address object (in the method ShutdownMSPCall) to shut down the MSP call object.
old-location: tapi3\cmspcallmultigraph_shutdown.htm
tech.root: Tapi
ms.assetid: cfcdf443-00c3-4cb5-abb1-1ec072272c0d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],ShutDown method, CMSPCallMultiGraph.ShutDown, CMSPCallMultiGraph::ShutDown, ShutDown, ShutDown method [TAPI 2.2], ShutDown method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_shutdown, mspcall/CMSPCallMultiGraph::ShutDown, tapi3.cmspcallmultigraph_shutdown
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
 - CMSPCallMultiGraph.ShutDown
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPCallMultiGraph::ShutDown


## -description


The 
<b>ShutDown</b> method is called by the MSP address object (in the method 
<a href="https://msdn.microsoft.com/6527db85-cad8-4b0d-977a-9ab8b047e44e">ShutdownMSPCall</a>) to shut down the MSP call object. Cancels the thread pool waits on the call's graph events. Releases the references on all the stream objects. Calls the shutdown method on all the stream objects. Acquires the lock in the function.


## -parameters






## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms726558(v=VS.85).aspx">CMSPCallMultiGraph</a>
 

 

