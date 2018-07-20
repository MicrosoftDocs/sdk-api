---
UID: NF:mspcall.CMSPCallBase.ShutDown
title: CMSPCallBase::ShutDown
author: windows-sdk-content
description: The ShutDown method is called by the MSPAddress object (in the method ShutdownMSPCall) to shut down the call.
old-location: tapi3\cmspcallbase_shutdown.htm
old-project: tapi
ms.assetid: eec5b712-5cee-41f7-819f-60815d5fba5c
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],ShutDown method, CMSPCallBase.ShutDown, CMSPCallBase::ShutDown, ShutDown, ShutDown method [TAPI 2.2], ShutDown method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_shutdown, mspcall/CMSPCallBase::ShutDown, tapi3.cmspcallbase_shutdown
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspcall.h
api_name:
 - CMSPCallBase.ShutDown
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPCallBase::ShutDown


## -description


The 
<b>ShutDown</b> method is called by the <b>MSPAddress</b> object (in the method 
<a href="https://msdn.microsoft.com/6527db85-cad8-4b0d-977a-9ab8b047e44e">ShutdownMSPCall</a>) to shut down the call. The derived class implementation should shut down all the streams on the call. (See also 
<a href="https://msdn.microsoft.com/cfcdf443-00c3-4cb5-abb1-1ec072272c0d">CMSPCallMultiGraph::ShutDown</a>.)


## -parameters






## -see-also




<a href="https://msdn.microsoft.com/77b53b66-38fa-4823-9051-e857da8a7dd7">CMSPCallBase</a>
 

 

