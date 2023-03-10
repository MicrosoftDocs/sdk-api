---
UID: NN:msp.ITPluggableTerminalEventSinkRegistration
title: ITPluggableTerminalEventSinkRegistration (msp.h)
description: The ITPluggableTerminalEventSinkRegistration (msp.h) interface registers and unregisters a client application for pluggable terminal events.
helpviewer_keywords: ["ITPluggableTerminalEventSinkRegistration","ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2]","ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2]","described","_tapi3_itpluggableterminaleventsinkregistration","msp/ITPluggableTerminalEventSinkRegistration","tapi3.itpluggableterminaleventsinkregistration"]
old-location: tapi3\itpluggableterminaleventsinkregistration.htm
tech.root: tapi3
ms.assetid: 4c8924bd-468e-458c-b16a-ac378fb4b69a
ms.date: 08/08/2022
ms.keywords: ITPluggableTerminalEventSinkRegistration, ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2], ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2],described, _tapi3_itpluggableterminaleventsinkregistration, msp/ITPluggableTerminalEventSinkRegistration, tapi3.itpluggableterminaleventsinkregistration
req.header: msp.h
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
 - ITPluggableTerminalEventSinkRegistration
 - msp/ITPluggableTerminalEventSinkRegistration
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
 - ITPluggableTerminalEventSinkRegistration
---

# ITPluggableTerminalEventSinkRegistration interface


## -description

The 
<b>ITPluggableTerminalEventSinkRegistration</b> interface registers and unregisters a client application for pluggable terminal events. The 
<b>ITPluggableTerminalEventSinkRegistration</b> interface is created by calling <b>QueryInterface</b> on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itterminal">ITTerminal</a>.

## -inheritance

The <b>ITPluggableTerminalEventSinkRegistration</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITPluggableTerminalEventSinkRegistration</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink">ITPluggableTerminalEventSink</a>
