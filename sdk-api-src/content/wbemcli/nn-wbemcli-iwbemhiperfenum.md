---
UID: NN:wbemcli.IWbemHiPerfEnum
title: IWbemHiPerfEnum (wbemcli.h)
description: Used in refresher operations to provide rapid access to enumerations of instance objects.
helpviewer_keywords: ["IWbemHiPerfEnum","IWbemHiPerfEnum interface [Windows Management Instrumentation]","IWbemHiPerfEnum interface [Windows Management Instrumentation]","described","_hmm_iwbemhiperfenum","wbemcli/IWbemHiPerfEnum","wmi.iwbemhiperfenum"]
old-location: wmi\iwbemhiperfenum.htm
tech.root: wmi
ms.assetid: 71ce1c89-446e-4137-9857-9d3c5921e0b7
ms.date: 12/05/2018
ms.keywords: IWbemHiPerfEnum, IWbemHiPerfEnum interface [Windows Management Instrumentation], IWbemHiPerfEnum interface [Windows Management Instrumentation],described, _hmm_iwbemhiperfenum, wbemcli/IWbemHiPerfEnum, wmi.iwbemhiperfenum
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
 - IWbemHiPerfEnum
 - wbemcli/IWbemHiPerfEnum
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
 - IWbemHiPerfEnum
---

# IWbemHiPerfEnum interface


## -description

The 
<b>IWbemHiPerfEnum</b> interface is used in refresher operations to provide rapid access to enumerations of instance objects. WMI provides an implementation of this interface, which it passes to providers when 
<a href="/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum">IWbemHiPerfProvider::CreateRefreshableEnum</a> is called, and it returns to clients when 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum">IWbemConfigureRefresher::AddEnum</a> is called.

Client applications can call only the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects">GetObjects</a> method of this interface. Attempts by client applications to call the other 
<b>IWbemHiPerfEnum</b> methods return WBEM_E_ACCESS_DENIED. Providers call these other methods to update the enumerators whenever a client calls 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">Refresh</a>.
<div class="alert"><b>Note</b>  This interface is not implemented by the user or by a provider under any circumstances. The implementation provided by WMI is the only one supported.</div><div> </div>

## -inheritance

The <b>IWbemHiPerfEnum</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemHiPerfEnum</b> also has these types of members:

## -see-also

<a href="/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="/windows/desktop/WmiSdk/accessing-wmi-preinstalled-performance-classes">Accessing WMI Preinstalled Performance Classes</a>



<a href="/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a>
