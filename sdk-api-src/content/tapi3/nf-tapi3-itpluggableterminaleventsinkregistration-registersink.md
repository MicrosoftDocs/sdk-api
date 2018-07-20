---
UID: NF:tapi3.ITPluggableTerminalEventSinkRegistration.RegisterSink
title: ITPluggableTerminalEventSinkRegistration::RegisterSink
author: windows-sdk-content
description: The RegisterSink method registers the application for pluggable terminal event notification.
old-location: tapi3\itpluggableterminaleventsinkregistration_registersink.htm
old-project: tapi
ms.assetid: 4887d299-8c63-4ead-b456-e80417e6ec56
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITPluggableTerminalEventSinkRegistration interface [TAPI 2.2],RegisterSink method, ITPluggableTerminalEventSinkRegistration.RegisterSink, ITPluggableTerminalEventSinkRegistration::RegisterSink, RegisterSink, RegisterSink method [TAPI 2.2], RegisterSink method [TAPI 2.2],ITPluggableTerminalEventSinkRegistration interface, _tapi3_itpluggableterminaleventsinkregistration_registersink, msp/ITPluggableTerminalEventSinkRegistration::RegisterSink, tapi3.itpluggableterminaleventsinkregistration_registersink
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: MSP_EVENT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITPluggableTerminalEventSinkRegistration.RegisterSink
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITPluggableTerminalEventSinkRegistration::RegisterSink


## -description


The 
<b>RegisterSink</b> method registers the application for pluggable terminal event notification.


## -parameters




### -param pEventSink [in]

Pointer to the 
<a href="https://msdn.microsoft.com/bcf64c78-aad2-4b53-b938-cc1fd373c8b4">ITPluggableTerminalEventSink</a> interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/bcf64c78-aad2-4b53-b938-cc1fd373c8b4">ITPluggableTerminalEventSink</a>



<a href="https://msdn.microsoft.com/4c8924bd-468e-458c-b16a-ac378fb4b69a">ITPluggableTerminalEventSinkRegistration</a>



<a href="https://msdn.microsoft.com/261ea39e-485f-4039-94b0-cd92f614c0a9">UnregisterSink</a>
 

 

