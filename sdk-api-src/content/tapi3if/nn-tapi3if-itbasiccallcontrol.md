---
UID: NN:tapi3if.ITBasicCallControl
title: ITBasicCallControl (tapi3if.h)
description: The ITBasicCallControl interface is used by the application to connect, answer, and perform basic telephony operations on a call object.
helpviewer_keywords: ["ITBasicCallControl","ITBasicCallControl interface [TAPI 2.2]","ITBasicCallControl interface [TAPI 2.2]","described","_tapi3_itbasiccallcontrol","tapi3.itbasiccallcontrol","tapi3if/ITBasicCallControl"]
old-location: tapi3\itbasiccallcontrol.htm
tech.root: tapi3
ms.assetid: a0b4c496-5ee8-4810-8170-8ea505c99f18
ms.date: 12/05/2018
ms.keywords: ITBasicCallControl, ITBasicCallControl interface [TAPI 2.2], ITBasicCallControl interface [TAPI 2.2],described, _tapi3_itbasiccallcontrol, tapi3.itbasiccallcontrol, tapi3if/ITBasicCallControl
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
 - ITBasicCallControl
 - tapi3if/ITBasicCallControl
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
 - ITBasicCallControl
---

# ITBasicCallControl interface


## -description

The 
<b>ITBasicCallControl</b> interface is used by the application to connect, answer, and perform basic telephony operations on a 
<a href="/windows/desktop/Tapi/call-object">call object</a>.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2">ITBasicCallControl2</a> interface is an extension of the 
<b>ITBasicCallControl</b> interface. 
<b>ITBasicCallControl2</b> supplies additional methods that allow an application to select a terminal onto a call. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall">ITAddress::CreateCall</a> method creates the 
<b>ITBasicCallControl</b> interface.

Note to programmers familiar with TAPI 2.1: The general function of this interface is similar to the TAPI 2.1 line functions. For example, the 
<a href="/windows/desktop/api/tapi/nf-tapi-lineanswer">lineAnswer</a> function and the 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-answer">ITBasicCallControl::Answer</a> method provide similar functionality.

## -inheritance

The <b>ITBasicCallControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITBasicCallControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol2">ITBasicCallControl2</a>
