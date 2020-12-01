---
UID: NF:mspcall.CMSPCallMultiGraph.Init
title: CMSPCallMultiGraph::Init (mspcall.h)
description: The Init method is called by the MSP address object (in the method CreateMSPCall) to initialize the MSP call object.
helpviewer_keywords: ["CMSPCallMultiGraph interface [TAPI 2.2]","Init method","CMSPCallMultiGraph.Init","CMSPCallMultiGraph::Init","Init","Init method [TAPI 2.2]","Init method [TAPI 2.2]","CMSPCallMultiGraph interface","_tapi3_cmspcallmultigraph_init","mspcall/CMSPCallMultiGraph::Init","tapi3.cmspcallmultigraph_init"]
old-location: tapi3\cmspcallmultigraph_init.htm
tech.root: tapi3
ms.assetid: ffb250b1-b66c-470b-ac73-91511623da00
ms.date: 12/05/2018
ms.keywords: CMSPCallMultiGraph interface [TAPI 2.2],Init method, CMSPCallMultiGraph.Init, CMSPCallMultiGraph::Init, Init, Init method [TAPI 2.2], Init method [TAPI 2.2],CMSPCallMultiGraph interface, _tapi3_cmspcallmultigraph_init, mspcall/CMSPCallMultiGraph::Init, tapi3.cmspcallmultigraph_init
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
 - CMSPCallMultiGraph::Init
 - mspcall/CMSPCallMultiGraph::Init
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
 - CMSPCallMultiGraph.Init
---

# CMSPCallMultiGraph::Init


## -description

The 
<b>Init</b> method is called by the MSP address object (in the method 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall">CreateMSPCall</a>) to initialize the MSP call object. The 
<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a> implementation initializes its members using the passed-in information. It calls 
<a href="/windows/desktop/api/mspaddr/nf-mspaddr-cmspaddress-mspaddressaddref">MSPAddressAddRef</a> on the MSP address object. Derived MSPs will want to override this method and call it in the overridden method; the overridden method should create the default streams based on the passed-in media types.

## -parameters

### -param pMSPAddress

Pointer to 
<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a> for call being initialized.

### -param htCall

The MSP's handle for the call being initialized

### -param dwReserved

Reserved parameter.

### -param dwMediaType

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media type</a> or types of call.

## -see-also

<a href="/windows/desktop/api/mspcall/nl-mspcall-cmspcallmultigraph">CMSPCallMultiGraph</a>