---
UID: NF:wbemcli.IWbemRefresher.Refresh
title: IWbemRefresher::Refresh (wbemcli.h)
description: The IWbemRefresher::Refresh method updates all refreshable objects, enumerators, and nested refreshers. The WMI Refresher calls this function in response to a client request to Refresh.
helpviewer_keywords: ["IWbemRefresher interface [Windows Management Instrumentation]","Refresh method","IWbemRefresher.Refresh","IWbemRefresher::Refresh","Refresh","Refresh method [Windows Management Instrumentation]","Refresh method [Windows Management Instrumentation]","IWbemRefresher interface","_hmm_iwbemrefresher_refresh","wbemcli/IWbemRefresher::Refresh","wmi.iwbemrefresher_refresh"]
old-location: wmi\iwbemrefresher_refresh.htm
tech.root: wmi
ms.assetid: 6de85040-c938-41dc-8240-0e21e89c7716
ms.date: 12/05/2018
ms.keywords: IWbemRefresher interface [Windows Management Instrumentation],Refresh method, IWbemRefresher.Refresh, IWbemRefresher::Refresh, Refresh, Refresh method [Windows Management Instrumentation], Refresh method [Windows Management Instrumentation],IWbemRefresher interface, _hmm_iwbemrefresher_refresh, wbemcli/IWbemRefresher::Refresh, wmi.iwbemrefresher_refresh
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
 - IWbemRefresher::Refresh
 - wbemcli/IWbemRefresher::Refresh
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
 - IWbemRefresher.Refresh
---

# IWbemRefresher::Refresh


## -description

The 
<b>IWbemRefresher::Refresh</b> method updates all refreshable objects, enumerators, and nested refreshers. The WMI Refresher calls this function in response to a client request to 
<b>Refresh</b>.

## -parameters

### -param lFlags [in]

Bitmask of flags that modify the behavior of this method.

If <b>WBEM_FLAG_REFRESH_AUTO_RECONNECT</b> is specified and if the connection is broken, the refresher attempts to reconnect to the provider automatically. This is the default behavior for this method.

If you do not want the refresher to attempt to reconnect to the provider, specify <b>WBEM_FLAG_REFRESH_NO_AUTO_RECONNECT</b>.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

When refreshing enumerators and objects, providers should take as little time as possible. Using the 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemobjectaccess">IWbemObjectAccess</a> methods and caching property handles for reuse can dramatically improve performance. When updating enumerators, a provider can either remove and re-instantiate all objects, or simply remove and add the changed instances. It is up to you to choose the best approach. In either case, caching instances can improve performance.

The provider should only access the objects and enumerators in a refresher in response to a call to 
<b>IWbemRefresher::Refresh</b>. It would, however, be perfectly valid to have a background thread polling for data with which to fill these objects, to prepare for when 
<b>Refresh</b> is called.


#### Examples

The following code example describes how to implement 
<b>Refresh</b>.


```cpp
HRESULT CMyHiPerfProviderRefresher::Refresh(
/* [in] */long lFlags
)
{
  // Run through all the objects and update their
  // data.

  // Now run through the enumerators.
  // Empty the enumerator and refill it.
   

  return WBEM_S_NO_ERROR;
}
```

## -see-also

<a href="/windows/desktop/WmiSdk/developing-a-wmi-provider">Developing a WMI Provider</a>



<a href="/windows/desktop/api/wbemprov/nn-wbemprov-iwbemhiperfprovider">IWbemHiPerfProvider</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a>



Making an Instance Provider into a High-Performance Provider



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Writing an Instance Provider</a>