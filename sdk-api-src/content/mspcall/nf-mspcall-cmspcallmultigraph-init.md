---
UID: NF:mspcall.CMSPCallMultiGraph.Init
title: CMSPCallMultiGraph::Init
author: windows-sdk-content
description: The Init method is called by the MSP address object (in the method CreateMSPCall) to initialize the MSP call object.
old-location: tapi3\cmspcallmultigraph_init.htm
old-project: tapi
ms.assetid: ffb250b1-b66c-470b-ac73-91511623da00
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],Init method, CMSPCallMultiGraph.Init, CMSPCallMultiGraph::Init, Init, Init method [TAPI 2.2], Init method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_init, mspcall/CMSPCallMultiGraph::Init, tapi3.cmspcallmultigraph_init
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
 - CMSPCallMultiGraph.Init
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# CMSPCallMultiGraph::Init


## -description


The 
<b>Init</b> method is called by the MSP address object (in the method 
<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>) to initialize the MSP call object. The 
<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a> implementation initializes its members using the passed-in information. It calls 
<a href="https://msdn.microsoft.com/74a68851-f1c2-41ed-94cd-ec043be0f0d1">MSPAddressAddRef</a> on the MSP address object. Derived MSPs will want to override this method and call it in the overridden method; the overridden method should create the default streams based on the passed-in media types.


## -parameters




### -param pMSPAddress

Pointer to 
<a href="https://msdn.microsoft.com/864bf814-43dd-4d2b-a5a7-fff12520accb">CMSPAddress</a> for call being initialized.


### -param htCall

The MSP's handle for the call being initialized


### -param dwReserved

Reserved parameter.


### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> or types of call.


## -see-also




<a href="https://msdn.microsoft.com/86512d40-380b-4e98-840d-b7be99a86623">CMSPCallMultiGraph</a>
 

 

