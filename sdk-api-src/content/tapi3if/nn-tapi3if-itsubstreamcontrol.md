---
UID: NN:tapi3if.ITSubStreamControl
title: ITSubStreamControl (tapi3if.h)
description: The ITSubStreamControl interface exposes methods that allow an application to enumerate, create, or remove substreams. Many MSPs do not support this interface.
helpviewer_keywords: ["ITSubStreamControl","ITSubStreamControl interface [TAPI 2.2]","ITSubStreamControl interface [TAPI 2.2]","described","_tapi3_itsubstreamcontrol","tapi3.itsubstreamcontrol","tapi3if/ITSubStreamControl"]
old-location: tapi3\itsubstreamcontrol.htm
tech.root: tapi3
ms.assetid: 17c5f2ba-d526-4b00-9649-8fd73d70bc79
ms.date: 12/05/2018
ms.keywords: ITSubStreamControl, ITSubStreamControl interface [TAPI 2.2], ITSubStreamControl interface [TAPI 2.2],described, _tapi3_itsubstreamcontrol, tapi3.itsubstreamcontrol, tapi3if/ITSubStreamControl
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
 - ITSubStreamControl
 - tapi3if/ITSubStreamControl
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
 - ITSubStreamControl
---

# ITSubStreamControl interface


## -description

The 
<b>ITSubStreamControl</b> interface exposes methods that allow an application to enumerate, create, or remove substreams. Many MSPs do not support this interface.

A pointer to this interface can be obtained by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the stream object.

## -inheritance

The <b>ITSubStreamControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITSubStreamControl</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
