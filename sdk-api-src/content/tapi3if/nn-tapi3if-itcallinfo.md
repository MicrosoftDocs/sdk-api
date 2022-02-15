---
UID: NN:tapi3if.ITCallInfo
title: ITCallInfo (tapi3if.h)
description: The ITCallInfo interface gets and sets a variety of information concerning a Call object. The ITAddress::get_Calls and IEnumCall::Next methods create the ITCallInfo interface.
helpviewer_keywords: ["ITCallInfo","ITCallInfo interface [TAPI 2.2]","ITCallInfo interface [TAPI 2.2]","described","_tapi3_itcallinfo","tapi3.itcallinfo","tapi3if/ITCallInfo"]
old-location: tapi3\itcallinfo.htm
tech.root: tapi3
ms.assetid: 5209d4a1-e05b-453e-8896-2dc71f0b9af0
ms.date: 12/05/2018
ms.keywords: ITCallInfo, ITCallInfo interface [TAPI 2.2], ITCallInfo interface [TAPI 2.2],described, _tapi3_itcallinfo, tapi3.itcallinfo, tapi3if/ITCallInfo
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
 - ITCallInfo
 - tapi3if/ITCallInfo
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
 - ITCallInfo
---

# ITCallInfo interface


## -description

The 
<b>ITCallInfo</b> interface gets and sets a variety of information concerning a 
<a href="/windows/desktop/Tapi/call-object">Call object</a>. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_calls">ITAddress::get_Calls</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumcall-next">IEnumCall::Next</a> methods create the 
<b>ITCallInfo</b> interface.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2">ITCallInfo2</a> interface is an extension of the 
<b>ITCallInfo</b> interface. 
<b>ITCallInfo2</b> provides additional methods that allow an application to set event filtering on a per-call basis.

For a table showing the relationships between TAPI 2 functions and  
<b>ITCallInfo</b> methods, see 
<a href="/windows/desktop/Tapi/tapi-2-x-to-tapi-3-x-cross-reference">TAPI 2.x to TAPI 3.x Cross-Reference</a>.

## -inheritance

The <b>ITCallInfo</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITCallInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/Tapi/call-object">Call Object</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo2">ITCallInfo2</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallinfo">LINECALLINFO</a>



<a href="/windows/desktop/api/tapi/ns-tapi-linecallstatus">LINECALLSTATUS</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallinfo">lineGetCallInfo</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetcallstatus">lineGetCallStatus</a>
