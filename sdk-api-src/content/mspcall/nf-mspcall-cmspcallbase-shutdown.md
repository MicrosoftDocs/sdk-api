---
UID: NF:mspcall.CMSPCallBase.ShutDown
title: CMSPCallBase::ShutDown (mspcall.h)
description: The ShutDown method is called by the MSPAddress object (in the method ShutdownMSPCall) to shut down the call.
helpviewer_keywords: ["CMSPCallBase interface [TAPI 2.2]","ShutDown method","CMSPCallBase.ShutDown","CMSPCallBase::ShutDown","ShutDown","ShutDown method [TAPI 2.2]","ShutDown method [TAPI 2.2]","CMSPCallBase interface","_tapi3_cmspcallbase_shutdown","mspcall/CMSPCallBase::ShutDown","tapi3.cmspcallbase_shutdown"]
old-location: tapi3\cmspcallbase_shutdown.htm
tech.root: tapi3
ms.assetid: eec5b712-5cee-41f7-819f-60815d5fba5c
ms.date: 12/05/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],ShutDown method, CMSPCallBase.ShutDown, CMSPCallBase::ShutDown, ShutDown, ShutDown method [TAPI 2.2], ShutDown method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_shutdown, mspcall/CMSPCallBase::ShutDown, tapi3.cmspcallbase_shutdown
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CMSPCallBase::ShutDown
 - mspcall/CMSPCallBase::ShutDown
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.ShutDown
---

# CMSPCallBase::ShutDown


## -description

The 
<b>ShutDown</b> method is called by the <b>MSPAddress</b> object (in the method 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall">ShutdownMSPCall</a>) to shut down the call. The derived class implementation should shut down all the streams on the call. (See also 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallmultigraph-shutdown">CMSPCallMultiGraph::ShutDown</a>.)



## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>
