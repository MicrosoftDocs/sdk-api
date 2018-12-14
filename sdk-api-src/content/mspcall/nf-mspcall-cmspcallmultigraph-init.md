---
UID: NF:mspcall.CMSPCallMultiGraph.Init
title: CMSPCallMultiGraph::Init
author: windows-sdk-content
description: The Init method is called by the MSP address object (in the method CreateMSPCall) to initialize the MSP call object.
old-location: tapi3\cmspcallmultigraph_init.htm
tech.root: tapi
ms.assetid: ffb250b1-b66c-470b-ac73-91511623da00
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],Init method, CMSPCallMultiGraph.Init, CMSPCallMultiGraph::Init, Init, Init method [TAPI 2.2], Init method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_init, mspcall/CMSPCallMultiGraph::Init, tapi3.cmspcallmultigraph_init
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - CMSPCallMultiGraph.Init
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CMSPCallMultiGraph::Init


## -description


The 
<b>Init</b> method is called by the MSP address object (in the method 
<a href="https://msdn.microsoft.com/56ed10e3-e711-43ae-aad6-65a5992fca0f">CreateMSPCall</a>) to initialize the MSP call object. The 
<a href="https://msdn.microsoft.com/en-us/library/ms726558(v=VS.85).aspx">CMSPCallMultiGraph</a> implementation initializes its members using the passed-in information. It calls 
<a href="https://msdn.microsoft.com/en-us/library/ms726447(v=VS.85).aspx">MSPAddressAddRef</a> on the MSP address object. Derived MSPs will want to override this method and call it in the overridden method; the overridden method should create the default streams based on the passed-in media types.


## -parameters




### -param pMSPAddress

Pointer to 
<a href="https://msdn.microsoft.com/en-us/library/ms726419(v=VS.85).aspx">CMSPAddress</a> for call being initialized.


### -param htCall

The MSP's handle for the call being initialized


### -param dwReserved

Reserved parameter.


### -param dwMediaType


<a href="https://msdn.microsoft.com/3e418c9a-a008-4b94-b5d2-7c2eccb3bf87">Media type</a> or types of call.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms726558(v=VS.85).aspx">CMSPCallMultiGraph</a>
 

 

