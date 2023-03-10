---
UID: NN:tapi3if.ITForwardInformation
title: ITForwardInformation (tapi3if.h)
description: The ITForwardInformation interface provides methods for setup and implementation of call forwarding.
helpviewer_keywords: ["ITForwardInformation","ITForwardInformation interface [TAPI 2.2]","ITForwardInformation interface [TAPI 2.2]","described","_tapi3_itforwardinformation","tapi3.itforwardinformation","tapi3if/ITForwardInformation"]
old-location: tapi3\itforwardinformation.htm
tech.root: tapi3
ms.assetid: 0e06cd0b-b95b-4853-b883-53146be084f0
ms.date: 12/05/2018
ms.keywords: ITForwardInformation, ITForwardInformation interface [TAPI 2.2], ITForwardInformation interface [TAPI 2.2],described, _tapi3_itforwardinformation, tapi3.itforwardinformation, tapi3if/ITForwardInformation
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
 - ITForwardInformation
 - tapi3if/ITForwardInformation
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
 - ITForwardInformation
---

# ITForwardInformation interface


## -description

The 
<b>ITForwardInformation</b> interface provides methods for setup and implementation of call forwarding. The forward information object is created by 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>. A pointer to an existing forward information object can be retrieved using 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>.

## -inheritance

The <b>ITForwardInformation</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITForwardInformation</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createforwardinfoobject">ITAddress::CreateForwardInfoObject</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward">ITAddress::Forward</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo">ITAddress::get_CurrentForwardInfo</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itforwardinformation2">ITForwardInformation2</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>
