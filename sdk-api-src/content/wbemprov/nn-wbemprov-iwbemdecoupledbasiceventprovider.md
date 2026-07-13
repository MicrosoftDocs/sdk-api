---
UID: NN:wbemprov.IWbemDecoupledBasicEventProvider
title: IWbemDecoupledBasicEventProvider (wbemprov.h)
description: The IWbemDecoupledBasicEventProvider interface is a cocreatable interface that registers decoupled providers with WMI. The object created should be passed into the pUnknown argument of IWbemDecoupledRegistrar::Register.
helpviewer_keywords: ["IWbemDecoupledBasicEventProvider","IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation]","IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation]","described","_hmm_iwbemdecoupledbasiceventprovider","wbemprov/IWbemDecoupledBasicEventProvider","wmi.iwbemdecoupledbasiceventprovider"]
old-location: wmi\iwbemdecoupledbasiceventprovider.htm
tech.root: wmi
ms.assetid: 71ce4f79-8168-47c5-a8b1-4286b34f7a31
ms.date: 12/05/2018
ms.keywords: IWbemDecoupledBasicEventProvider, IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation], IWbemDecoupledBasicEventProvider interface [Windows Management Instrumentation],described, _hmm_iwbemdecoupledbasiceventprovider, wbemprov/IWbemDecoupledBasicEventProvider, wmi.iwbemdecoupledbasiceventprovider
req.header: wbemprov.h
req.include-header: Wbemidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wbemprov.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wbemuuid.lib
req.dll: Wmidcprv.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemDecoupledBasicEventProvider
 - wbemprov/IWbemDecoupledBasicEventProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmidcprv.dll
api_name:
 - IWbemDecoupledBasicEventProvider
---

# IWbemDecoupledBasicEventProvider interface


## -description

The 
<b>IWbemDecoupledBasicEventProvider</b> interface is a cocreatable interface that  registers decoupled providers with WMI. The object created should be passed into the <i>pUnknown </i> argument of 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemdecoupledregistrar-register">IWbemDecoupledRegistrar::Register</a>.

## -inheritance

The <b>IWbemDecoupledBasicEventProvider</b> interface inherits from <a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemdecoupledregistrar">IWbemDecoupledRegistrar</a>. <b>IWbemDecoupledBasicEventProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemdecoupledregistrar">IWbemDecoupledRegistrar</a>



<a href="/windows/desktop/WmiSdk/incorporating-a-provider-in-an-application">Incorporating a Provider in an Application</a>
