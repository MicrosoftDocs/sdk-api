---
UID: NN:tapi3if.ITTerminal
title: ITTerminal (tapi3if.h)
description: The ITTerminal interface is the base interface for a Terminal object.
helpviewer_keywords: ["ITTerminal","ITTerminal interface [TAPI 2.2]","ITTerminal interface [TAPI 2.2]","described","_tapi3_itterminal","tapi3.itterminal","tapi3if/ITTerminal"]
old-location: tapi3\itterminal.htm
tech.root: tapi3
ms.assetid: 38bc30fa-3e4e-417a-9d04-931ba2451fa4
ms.date: 12/05/2018
ms.keywords: ITTerminal, ITTerminal interface [TAPI 2.2], ITTerminal interface [TAPI 2.2],described, _tapi3_itterminal, tapi3.itterminal, tapi3if/ITTerminal
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
 - ITTerminal
 - tapi3if/ITTerminal
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
 - ITTerminal
---

# ITTerminal interface


## -description

The 
<b>ITTerminal</b> interface is the base interface for a 
<a href="/windows/desktop/Tapi/terminal-object">Terminal object</a>. This object, and the interface, is available only when an MSP exists. It provides methods that allow an application to obtain information such as terminal class and media supported. The following methods create the 
<b>ITTerminal</b> interface:


<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol2-requestterminal">ITBasicCallControl2::RequestTerminal</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itterminalsupport-createterminal">ITTerminalSupport::CreateTerminal</a>



<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ienumterminal-next">IEnumTerminal::Next</a>

## -inheritance

The <b>ITTerminal</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITTerminal</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/Tapi/terminal-object">Terminal Object</a>



<a href="/windows/desktop/Tapi/terminal-object-interfaces">Terminal Object Interfaces</a>
