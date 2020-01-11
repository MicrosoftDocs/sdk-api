---
UID: NF:mspcall.CMSPCallBase.Init
title: CMSPCallBase::Init (mspcall.h)
description: The Init method is called by the MSP address object (in the method CreateMSPCall) to initialize the MSP call object. The derived class should initialize its members using the passed-in information.
old-location: tapi3\cmspcallbase_init.htm
tech.root: Tapi
ms.assetid: bda49b8e-4ae5-4cf9-ae61-44fbf41e2cda
ms.date: 12/05/2018
ms.keywords: CMSPCallBase interface [TAPI 2.2],Init method, CMSPCallBase.Init, CMSPCallBase::Init, Init, Init method [TAPI 2.2], Init method [TAPI 2.2],CMSPCallBase interface, _tapi3_cmspcallbase_init, mspcall/CMSPCallBase::Init, tapi3.cmspcallbase_init
f1_keywords:
- mspcall/CMSPCallBase.Init
dev_langs:
- c++
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
- CMSPCallBase.Init
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CMSPCallBase::Init


## -description


The 
<b>Init</b> method is called by the MSP address object (in the method 
<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall">CreateMSPCall</a>) to initialize the MSP call object. The derived class should initialize its members using the passed-in information.


## -parameters




### -param pMSPAddress

Pointer to MSP call object to be initialized.


### -param htCall

The MSP handle for the call.


### -param dwReserved

Reserved.


### -param dwMediaType


<a href="https://docs.microsoft.com/windows/desktop/Tapi/tapimediatype--constants">Media type</a> or types of call.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nl-mspcall-cmspcallbase">CMSPCallBase</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mspcall/nf-mspcall-cmspcallmultigraph-init">CMSPCallMultiGraph::Init</a>



<a href="https://docs.microsoft.com/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall">CreateMSPCall</a>
 

 

