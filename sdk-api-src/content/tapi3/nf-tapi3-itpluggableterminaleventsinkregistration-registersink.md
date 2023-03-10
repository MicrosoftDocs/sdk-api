---
UID: NF:tapi3.ITPluggableTerminalEventSinkRegistration.RegisterSink
title: ITPluggableTerminalEventSinkRegistration::RegisterSink (tapi3.h)
description: The ITPluggableTerminalEventSinkRegistration::RegisterSink (tapi3.h) method registers the application for pluggable terminal event notification.
helpviewer_keywords: ["ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2]","RegisterSink method","ITPluggableTerminalEventSinkRegistration.RegisterSink","ITPluggableTerminalEventSinkRegistration::RegisterSink","RegisterSink","RegisterSink method [TAPI 2.2]","RegisterSink method [TAPI 2.2]","ITPluggableTerminalEventSinkRegistration interface","_tapi3_itpluggableterminaleventsinkregistration_registersink","msp/ITPluggableTerminalEventSinkRegistration::RegisterSink","tapi3.itpluggableterminaleventsinkregistration_registersink"]
old-location: tapi3\itpluggableterminaleventsinkregistration_registersink.htm
tech.root: tapi3
ms.assetid: 4887d299-8c63-4ead-b456-e80417e6ec56
ms.date: 08/10/2022
ms.keywords: ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2],RegisterSink method, ITPluggableTerminalEventSinkRegistration.RegisterSink, ITPluggableTerminalEventSinkRegistration::RegisterSink, RegisterSink, RegisterSink method [TAPI 2.2], RegisterSink method [TAPI 2.2],ITPluggableTerminalEventSinkRegistration interface, _tapi3_itpluggableterminaleventsinkregistration_registersink, msp/ITPluggableTerminalEventSinkRegistration::RegisterSink, tapi3.itpluggableterminaleventsinkregistration_registersink
req.header: tapi3.h
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
 - ITPluggableTerminalEventSinkRegistration::RegisterSink
 - tapi3/ITPluggableTerminalEventSinkRegistration::RegisterSink
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
 - ITPluggableTerminalEventSinkRegistration.RegisterSink
---

# ITPluggableTerminalEventSinkRegistration::RegisterSink


## -description

The 
<b>RegisterSink</b> method registers the application for pluggable terminal event notification.

## -parameters

### -param pEventSink [in]

Pointer to the 
<a href="/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink">ITPluggableTerminalEventSink</a> interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsink">ITPluggableTerminalEventSink</a>



<a href="/windows/desktop/api/msp/nn-msp-itpluggableterminaleventsinkregistration">ITPluggableTerminalEventSinkRegistration</a>



<a href="/windows/desktop/api/msp/nf-msp-itpluggableterminaleventsinkregistration-unregistersink">UnregisterSink</a>
