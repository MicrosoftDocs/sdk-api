---
UID: NF:mspaddr.CreateMSPCallHelper
title: CreateMSPCallHelper function (mspaddr.h)
description: The CreateMSPCallHelper helper template function is called in the derived class' implementation of CreateMSPCall.
helpviewer_keywords: ["CMSPAddress object [TAPI 2.2]","CreateMSPCallHelper method","CMSPAddress.CreateMSPCallHelper","CreateMSPCallHelper","CreateMSPCallHelper method [TAPI 2.2]","CreateMSPCallHelper method [TAPI 2.2]","CMSPAddress object","_tapi3_cmspaddress_createmspcallhelper","tapi3.cmspaddress_createmspcallhelper"]
old-location: tapi3\cmspaddress_createmspcallhelper.htm
tech.root: tapi3
ms.assetid: 1e894d26-de19-4c24-b4e6-58c0b4c9d5ee
ms.date: 12/05/2018
ms.keywords: CMSPAddress object [TAPI 2.2],CreateMSPCallHelper method, CMSPAddress.CreateMSPCallHelper, CreateMSPCallHelper, CreateMSPCallHelper method [TAPI 2.2], CreateMSPCallHelper method [TAPI 2.2],CMSPAddress object, _tapi3_cmspaddress_createmspcallhelper, tapi3.cmspaddress_createmspcallhelper
req.header: mspaddr.h
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
 - CreateMSPCallHelper
 - mspaddr/CreateMSPCallHelper
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mspaddr.h
api_name:
 - CMSPAddress.CreateMSPCallHelper
---

# CreateMSPCallHelper function


## -description

The 
<b>CreateMSPCallHelper</b> helper template function is called in the derived class' implementation of 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall">CreateMSPCall</a>. It checks all of the arguments for validity, including the media type argument (via the address object method 
<a href="/windows/desktop/api/mspaddr/nf-mspaddr-cmspaddress-isvalidsetofmediatypes">IsValidSetOfMediaTypes</a>; see above). It sets up the aggregation between the MSP call object and the TAPI call object using the <b>CComAggObject</b> ATL class template. It then calls the 
<a href="/windows/desktop/api/mspcall/nf-mspcall-cmspcallbase-init">Init</a> method on the MSP call object.

## -parameters

### -param pCMSPAddress

Pointer to 
<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a> interface for call.

### -param htCall

Handle for MSP.

### -param dwReserved

Reserved parameter, not currently used.

### -param dwMediaType

<a href="/windows/desktop/Tapi/tapimediatype--constants">Media types</a> desired for call.

### -param pOuterUnknown

Pointer to <b>IUnknown</b> interface for TAPI call object.

### -param ppMSPCall

Pointer to <b>IUnknown</b> interface for MSP call object.

### -param ppCMSPCall

Pointer to templated MSP call class, type implementation dependent.

### -param unnamedParam8

TBD

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a>



<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall">CreateMSPCall</a>