---
UID: NN:tapi3if.ITLegacyCallMediaControl
title: ITLegacyCallMediaControl (tapi3if.h)
description: The ITLegacyCallMediaControl interface supports legacy applications that must communicate directly with a device. This interface is exposed on the Call Object and can be created by calling QueryInterface on ITBasicCallControl.
helpviewer_keywords: ["ITLegacyCallMediaControl","ITLegacyCallMediaControl interface [TAPI 2.2]","ITLegacyCallMediaControl interface [TAPI 2.2]","described","_tapi3_itlegacycallmediacontrol","tapi3.itlegacycallmediacontrol","tapi3if/ITLegacyCallMediaControl"]
old-location: tapi3\itlegacycallmediacontrol.htm
tech.root: tapi3
ms.assetid: 73288c46-6c6d-4938-9bb7-4d94acfc67f6
ms.date: 12/05/2018
ms.keywords: ITLegacyCallMediaControl, ITLegacyCallMediaControl interface [TAPI 2.2], ITLegacyCallMediaControl interface [TAPI 2.2],described, _tapi3_itlegacycallmediacontrol, tapi3.itlegacycallmediacontrol, tapi3if/ITLegacyCallMediaControl
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
 - ITLegacyCallMediaControl
 - tapi3if/ITLegacyCallMediaControl
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
 - ITLegacyCallMediaControl
---

# ITLegacyCallMediaControl interface


## -description

The 
<b>ITLegacyCallMediaControl</b> interface supports legacy applications that must communicate directly with a device. This interface is exposed on the 
<a href="/windows/desktop/Tapi/call-object">Call Object</a> and can be created by calling <b>QueryInterface</b> on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol">ITBasicCallControl</a>.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a> interface is an extension of the 
<b>ITLegacyCallMediaControl</b> interface. 
<b>ITLegacyCallMediaControl2</b> provides additional methods, primarily for tone detection and generation.

## -inheritance

The <b>ITLegacyCallMediaControl</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITLegacyCallMediaControl</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacycallmediacontrol2">ITLegacyCallMediaControl2</a>
