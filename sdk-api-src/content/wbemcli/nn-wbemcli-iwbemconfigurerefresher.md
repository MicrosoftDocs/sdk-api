---
UID: NN:wbemcli.IWbemConfigureRefresher
title: IWbemConfigureRefresher (wbemcli.h)
description: The IWbemConfigureRefresher interface is used by client code to add enumerators, objects, and nested refreshers into a refresher.
helpviewer_keywords: ["IWbemConfigureRefresher","IWbemConfigureRefresher interface [Windows Management Instrumentation]","IWbemConfigureRefresher interface [Windows Management Instrumentation]","described","_hmm_iwbemconfigurerefresher","wbemcli/IWbemConfigureRefresher","wmi.iwbemconfigurerefresher"]
old-location: wmi\iwbemconfigurerefresher.htm
tech.root: wmi
ms.assetid: 9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43
ms.date: 12/05/2018
ms.keywords: IWbemConfigureRefresher, IWbemConfigureRefresher interface [Windows Management Instrumentation], IWbemConfigureRefresher interface [Windows Management Instrumentation],described, _hmm_iwbemconfigurerefresher, wbemcli/IWbemConfigureRefresher, wmi.iwbemconfigurerefresher
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
 - IWbemConfigureRefresher
 - wbemcli/IWbemConfigureRefresher
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
 - IWbemConfigureRefresher
---

# IWbemConfigureRefresher interface


## -description

The 
<b>IWbemConfigureRefresher</b> interface is used by client code to add enumerators, objects, and nested refreshers into a refresher.

Users and providers should never implement this interface. The implementation provided by WMI is the only one that is supported.

By providing a native implementation of this interface, WMI allows client code to easily configure refreshers. You can access the 
<b>IWbemConfigureRefresher</b> interface by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on <b>IID_IWbemConfigureRefresher</b> on the object returned by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> on <b>CLSID_WbemRefresher</b>.

## -inheritance

The <b>IWbemConfigureRefresher</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemConfigureRefresher</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemconfigurerefresher">IWbemConfigureRefresher</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Making an Instance Provider into a High-Performance Provider</a>



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>
