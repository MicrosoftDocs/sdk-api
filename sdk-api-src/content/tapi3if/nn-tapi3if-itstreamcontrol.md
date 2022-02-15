---
UID: NN:tapi3if.ITStreamControl
title: ITStreamControl (tapi3if.h)
description: The ITStreamControl interface represents the media streaming features of a call and exposes methods that allow an application to enumerate, create, or remove streams.
helpviewer_keywords: ["ITStreamControl","ITStreamControl interface [TAPI 2.2]","ITStreamControl interface [TAPI 2.2]","described","_tapi3_itstreamcontrol","tapi3.itstreamcontrol","tapi3if/ITStreamControl"]
old-location: tapi3\itstreamcontrol.htm
tech.root: tapi3
ms.assetid: 12b9457a-7afb-4348-93a2-28728c673929
ms.date: 12/05/2018
ms.keywords: ITStreamControl, ITStreamControl interface [TAPI 2.2], ITStreamControl interface [TAPI 2.2],described, _tapi3_itstreamcontrol, tapi3.itstreamcontrol, tapi3if/ITStreamControl
req.header: tapi3if.h
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
 - ITStreamControl
 - tapi3if/ITStreamControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3if.h
api_name:
 - ITStreamControl
---

# ITStreamControl interface


## -description

The 
<b>ITStreamControl</b> interface represents the media streaming features of a call and exposes methods that allow an application to enumerate, create, or remove streams.

If this interface exists, a TAPI application acquires a pointer to this interface by performing a <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on any call interface, such as 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a>. This interface is not available if an MSP is not involved in the current call session.

Internal to the TAPI DLL, this interface is implemented by the MSP's call object, which is created in the 
<a href="/windows/desktop/api/msp/nf-msp-itmspaddress-createmspcall">ITMSPAddress::CreateMSPCall</a> method. TAPI then aggregates this interface onto the TAPI call object and exposes it to TAPI applications.

## -inheritance

The <b>ITStreamControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITStreamControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
