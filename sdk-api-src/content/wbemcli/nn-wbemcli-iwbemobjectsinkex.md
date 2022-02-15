---
UID: NN:wbemcli.IWbemObjectSinkEx
title: IWbemObjectSinkEx (wbemcli.h)
description: Creates a sink interface that can receive all types of notifications within the WMI programming model.
helpviewer_keywords: ["IWbemObjectSinkEx","IWbemObjectSinkEx interface [Windows Management Instrumentation]","IWbemObjectSinkEx interface [Windows Management Instrumentation]","described","wbemcli/IWbemObjectSinkEx","wmi.iwbemobjectsinkex"]
old-location: wmi\iwbemobjectsinkex.htm
tech.root: wmi
ms.assetid: f22b21f8-5191-480d-8471-3d5fc82ba060
ms.date: 12/05/2018
ms.keywords: IWbemObjectSinkEx, IWbemObjectSinkEx interface [Windows Management Instrumentation], IWbemObjectSinkEx interface [Windows Management Instrumentation],described, wbemcli/IWbemObjectSinkEx, wmi.iwbemobjectsinkex
req.header: wbemcli.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Fastprox.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemObjectSinkEx
 - wbemcli/IWbemObjectSinkEx
dev_langs:
 - c++
topic_type:
 - kbSyntax
api_type:
 - <TBD>
api_location:
api_name:
 - IWbemObjectSinkEx
---

# IWbemObjectSinkEx interface


## -description

Creates a sink interface that can receive all types of notifications within the WMI programming model. Clients must implement this interface to receive both the results of the 
<a href="/windows/desktop/WmiSdk/making-an-asynchronous-call-with-c--">asynchronous methods</a> of 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices">IWbemServices</a>, and specific types of event notifications. Providers use, but do not implement this interface to provide events and objects to WMI.

## -inheritance

The <b>IWbemObjectSinkEx</b> interface inherits from <b>IWbemObjectSink</b>. <b>IWbemObjectSinkEx</b> also has these types of members:

