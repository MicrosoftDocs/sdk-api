---
UID: NN:wbemprov.IWbemHiPerfProvider
title: IWbemHiPerfProvider (wbemprov.h)
description: Enables providers to supply refreshable objects and enumerators.
helpviewer_keywords: ["IWbemHiPerfProvider","IWbemHiPerfProvider interface [Windows Management Instrumentation]","IWbemHiPerfProvider interface [Windows Management Instrumentation]","described","_hmm_iwbemhiperfprovider","wbemprov/IWbemHiPerfProvider","wmi.iwbemhiperfprovider"]
old-location: wmi\iwbemhiperfprovider.htm
tech.root: wmi
ms.assetid: eb0d12c0-d746-4bae-b47d-50350d33447a
ms.date: 12/05/2018
ms.keywords: IWbemHiPerfProvider, IWbemHiPerfProvider interface [Windows Management Instrumentation], IWbemHiPerfProvider interface [Windows Management Instrumentation],described, _hmm_iwbemhiperfprovider, wbemprov/IWbemHiPerfProvider, wmi.iwbemhiperfprovider
req.header: wbemprov.h
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
req.dll: Wmiprvsd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemHiPerfProvider
 - wbemprov/IWbemHiPerfProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wmiprvsd.dll
api_name:
 - IWbemHiPerfProvider
---

# IWbemHiPerfProvider interface


## -description

The 
<b>IWbemHiPerfProvider</b> interface enables providers to supply refreshable objects and enumerators. High-performance providers can be loaded in-process to either WMI or a client process. When the provider is loaded in-process to a client process, it uses the CLSID specified as the <b>ClientLoadableCLSID</b> value in the <a href="/windows/desktop/WmiSdk/--win32provider">__Win32Provider</a>  representing the provider instance definition.

## -inheritance

The <b>IWbemHiPerfProvider</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemHiPerfProvider</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="/windows/desktop/WmiSdk/accessing-wmi-preinstalled-performance-classes">Accessing WMI Preinstalled Performance Classes</a>



<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a>



Making an Instance Provider into a High-Performance Provider



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Writing an Instance Provider</a>
