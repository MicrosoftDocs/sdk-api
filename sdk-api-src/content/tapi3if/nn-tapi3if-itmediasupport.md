---
UID: NN:tapi3if.ITMediaSupport
title: ITMediaSupport (tapi3if.h)
description: The ITMediaSupport interface provides methods that allow an application to discover the media support capabilities for an Address Object that exposes this interface.
helpviewer_keywords: ["ITMediaSupport","ITMediaSupport interface [TAPI 2.2]","ITMediaSupport interface [TAPI 2.2]","described","_tapi3_itmediasupport","tapi3.itmediasupport","tapi3if/ITMediaSupport"]
old-location: tapi3\itmediasupport.htm
tech.root: tapi3
ms.assetid: 196995f1-b8d0-4ec1-b94e-61a02a258087
ms.date: 12/05/2018
ms.keywords: ITMediaSupport, ITMediaSupport interface [TAPI 2.2], ITMediaSupport interface [TAPI 2.2],described, _tapi3_itmediasupport, tapi3.itmediasupport, tapi3if/ITMediaSupport
req.header: tapi3if.h
req.include-header: Tapi3.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITMediaSupport
 - tapi3if/ITMediaSupport
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITMediaSupport
---

# ITMediaSupport interface


## -description

The 
<b>ITMediaSupport</b> interface provides methods that allow an application to discover the media support capabilities for an 
<a href="/windows/desktop/Tapi/address-object">Address Object</a> that exposes this interface. A pointer to this interface can be obtained by calling <b>QueryInterface</b> using any address interface pointer, such as 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>.

## -inheritance

The <b>ITMediaSupport</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITMediaSupport</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport">ITTerminalSupport</a>
