---
UID: NN:tapi3if.IEnumCall
title: IEnumCall (tapi3if.h)
description: The IEnumCall interface provides COM-standard enumeration methods for the ITCallInfo interface. The ITCallHub::EnumerateCalls and ITAddress::EnumerateCalls methods return a pointer to IEnumCall.
helpviewer_keywords: ["IEnumCall","IEnumCall interface [TAPI 2.2]","IEnumCall interface [TAPI 2.2]","described","_tapi3_ienumcall","tapi3.ienumcall","tapi3if/IEnumCall"]
old-location: tapi3\ienumcall.htm
tech.root: tapi3
ms.assetid: 418c1005-98f0-406f-a85c-c08adb269b9f
ms.date: 12/05/2018
ms.keywords: IEnumCall, IEnumCall interface [TAPI 2.2], IEnumCall interface [TAPI 2.2],described, _tapi3_ienumcall, tapi3.ienumcall, tapi3if/IEnumCall
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
 - IEnumCall
 - tapi3if/IEnumCall
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
 - IEnumCall
---

# IEnumCall interface


## -description

The 
<b>IEnumCall</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo">ITCallInfo</a> interface. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itcallhub-enumeratecalls">ITCallHub::EnumerateCalls</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-enumeratecalls">ITAddress::EnumerateCalls</a> methods return a pointer to 
<b>IEnumCall</b>.

The 
<b>IEnumCall</b> interface is hidden from Visual Basic and scripting languages.

## -inheritance

The <b>IEnumCall</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumCall</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>
