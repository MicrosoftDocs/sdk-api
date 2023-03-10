---
UID: NN:wbemcli.IWbemRefresher
title: IWbemRefresher (wbemcli.h)
description: Provides an entry point through which refreshable objects such as enumerators or refresher objects, can be refreshed.
helpviewer_keywords: ["IWbemRefresher","IWbemRefresher interface [Windows Management Instrumentation]","IWbemRefresher interface [Windows Management Instrumentation]","described","WbemRefresher","_hmm_iwbemrefresher","wbemcli/IWbemRefresher","wmi.iwbemrefresher"]
old-location: wmi\iwbemrefresher.htm
tech.root: wmi
ms.assetid: cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed
ms.date: 12/05/2018
ms.keywords: IWbemRefresher, IWbemRefresher interface [Windows Management Instrumentation], IWbemRefresher interface [Windows Management Instrumentation],described, WbemRefresher, _hmm_iwbemrefresher, wbemcli/IWbemRefresher, wmi.iwbemrefresher
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWbemRefresher
 - wbemcli/IWbemRefresher
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wbemuuid.lib
 - Wbemuuid.dll
api_name:
 - IWbemRefresher
 - WbemRefresher
---

# IWbemRefresher interface


## -description

The 
<b>IWbemRefresher</b> interface provides an entry point through which refreshable objects such as enumerators or refresher objects, can be refreshed. Implementers of 
<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a> must provide an implementation of this interface.

WMI supplies a client implementation of this interface. Clients can access this interface by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> on <b>CLSID_WbemRefresher</b>. This is the only supported implementation on the client.

## -inheritance

The <b>IWbemRefresher</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemRefresher</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemconfigurerefresher">IWbemConfigureRefresher</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Making an Instance Provider into a High-Performance Provider</a>



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>



<a href="/windows/desktop/WmiSdk/writing-an-instance-provider">Writing an Instance Provider</a>
