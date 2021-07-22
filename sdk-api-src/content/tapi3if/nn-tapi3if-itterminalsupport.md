---
UID: NN:tapi3if.ITTerminalSupport
title: ITTerminalSupport (tapi3if.h)
description: The ITTerminalSupport interface is exposed on an Address object only if an MSP exists. The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required Terminal objects.
helpviewer_keywords: ["ITTerminalSupport","ITTerminalSupport interface [TAPI 2.2]","ITTerminalSupport interface [TAPI 2.2]","described","_tapi3_itterminalsupport","tapi3.itterminalsupport","tapi3if/ITTerminalSupport"]
old-location: tapi3\itterminalsupport.htm
tech.root: tapi3
ms.assetid: 8669324a-5c2c-4ed8-be24-a0c71fbb8c01
ms.date: 12/05/2018
ms.keywords: ITTerminalSupport, ITTerminalSupport interface [TAPI 2.2], ITTerminalSupport interface [TAPI 2.2],described, _tapi3_itterminalsupport, tapi3.itterminalsupport, tapi3if/ITTerminalSupport
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
 - ITTerminalSupport
 - tapi3if/ITTerminalSupport
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
 - ITTerminalSupport
---

# ITTerminalSupport interface


## -description

The 
<b>ITTerminalSupport</b> interface is exposed on an 
<a href="/windows/desktop/Tapi/address-object">Address object</a> only if an MSP exists. The methods of this interface allow an application to discover available terminals and/or create one, and get pointers to required 
<a href="/windows/desktop/Tapi/terminal-object">Terminal objects</a>.

An 
tapi3.itterminalsupport pointer can be obtained by calling 
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on any Address interface, such as 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>. If E_NOINTERFACE is returned, the service provider associated with the address does not support media controls.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2">ITTerminalSupport2</a> interface is derived from the 
<b>ITTerminalSupport</b> interface. 
<b>ITTerminalSupport2</b> supports the retrieval of information about pluggable terminal classes and superclasses by C, C++, and scripting applications.

## -inheritance

The <b>ITTerminalSupport</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTerminalSupport</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/address-object">Address Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminalsupport2">ITTerminalSupport2</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>
