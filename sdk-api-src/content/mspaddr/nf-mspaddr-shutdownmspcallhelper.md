---
UID: NF:mspaddr.ShutdownMSPCallHelper
title: ShutdownMSPCallHelper function (mspaddr.h)
description: The ShutdownMSPCallHelper helper template function is called in the derived class' implementation of ShutdownMSPCall.
helpviewer_keywords: ["CMSPAddress object [TAPI 2.2]","ShutdownMSPCallHelper method","CMSPAddress.ShutdownMSPCallHelper","ShutdownMSPCallHelper","ShutdownMSPCallHelper method [TAPI 2.2]","ShutdownMSPCallHelper method [TAPI 2.2]","CMSPAddress object","_tapi3_cmspaddress_shutdownmspcallhelper","tapi3.cmspaddress_shutdownmspcallhelper"]
old-location: tapi3\cmspaddress_shutdownmspcallhelper.htm
tech.root: tapi3
ms.assetid: 66f7b743-6100-45b9-98b0-3bacfcffed15
ms.date: 12/05/2018
ms.keywords: CMSPAddress object [TAPI 2.2],ShutdownMSPCallHelper method, CMSPAddress.ShutdownMSPCallHelper, ShutdownMSPCallHelper, ShutdownMSPCallHelper method [TAPI 2.2], ShutdownMSPCallHelper method [TAPI 2.2],CMSPAddress object, _tapi3_cmspaddress_shutdownmspcallhelper, tapi3.cmspaddress_shutdownmspcallhelper
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
 - ShutdownMSPCallHelper
 - mspaddr/ShutdownMSPCallHelper
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
 - CMSPAddress.ShutdownMSPCallHelper
---

# ShutdownMSPCallHelper function


## -description

The 
<b>ShutdownMSPCallHelper</b> helper template function is called in the derived class' implementation of 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-shutdownmspcall">ShutdownMSPCall</a>. It manipulates the passed-in aggregated TAPI call object Unknown pointer via dynamic casts to obtain a pointer to the inner MSP call object, and then calls the 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-shutdown">Shutdown</a> method on the MSP call object (see below).

## -parameters

### -param pUnknown

Pointer to IUnknown on aggregated TAPI call object.

### -param ppCMSPCall

Pointer to templated MSP call class, type implementation dependent.

### -param unnamedParam3

TBD

## -see-also

<a href="/windows/desktop/api/mspaddr/nl-mspaddr-cmspaddress">CMSPAddress</a>