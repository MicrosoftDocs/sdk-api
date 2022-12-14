---
UID: NN:tapi3if.ITStaticAudioTerminal
title: ITStaticAudioTerminal (tapi3if.h)
description: The ITStaticAudioTerminal interface is an interface that TAPI 3.1 MSPs must expose on all static audio terminals. The interface defines methods on static audio terminal objects that are needed to support phone devices.
helpviewer_keywords: ["ITStaticAudioTerminal","ITStaticAudioTerminal interface [TAPI 2.2]","ITStaticAudioTerminal interface [TAPI 2.2]","described","_tapi3_itstaticaudioterminal","tapi3.itstaticaudioterminal","tapi3if/ITStaticAudioTerminal"]
old-location: tapi3\itstaticaudioterminal.htm
tech.root: tapi3
ms.assetid: 154c07b6-c693-469d-819a-f6d2d2afd744
ms.date: 12/05/2018
ms.keywords: ITStaticAudioTerminal, ITStaticAudioTerminal interface [TAPI 2.2], ITStaticAudioTerminal interface [TAPI 2.2],described, _tapi3_itstaticaudioterminal, tapi3.itstaticaudioterminal, tapi3if/ITStaticAudioTerminal
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
 - ITStaticAudioTerminal
 - tapi3if/ITStaticAudioTerminal
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
 - ITStaticAudioTerminal
---

# ITStaticAudioTerminal interface


## -description

The 
<b>ITStaticAudioTerminal</b> interface is an interface that TAPI 3.1 MSPs must expose on all static audio terminals. The interface defines methods on static audio terminal objects that are needed to support phone devices.

If an MSP's audio terminals are for devices that are not accessible via standard audio APIs, then a 
<a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>(IID_ITStaticAudioTerminal) should return E_NOINTERFACE, and it will be impossible to associate a USB phone with any of these audio terminals in TAPI 3.1.

## -inheritance

The <b>ITStaticAudioTerminal</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITStaticAudioTerminal</b> also has these types of members:

