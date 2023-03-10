---
UID: NF:wbemcli.IWbemConfigureRefresher.AddRefresher
title: IWbemConfigureRefresher::AddRefresher (wbemcli.h)
description: The IWbemConfigureRefresher::AddRefresher method adds a refresher to a refresher.
helpviewer_keywords: ["AddRefresher","AddRefresher method [Windows Management Instrumentation]","AddRefresher method [Windows Management Instrumentation]","IWbemConfigureRefresher interface","IWbemConfigureRefresher interface [Windows Management Instrumentation]","AddRefresher method","IWbemConfigureRefresher.AddRefresher","IWbemConfigureRefresher::AddRefresher","_hmm_iwbemconfigurerefresher_addrefresher","wbemcli/IWbemConfigureRefresher::AddRefresher","wmi.iwbemconfigurerefresher_addrefresher"]
old-location: wmi\iwbemconfigurerefresher_addrefresher.htm
tech.root: wmi
ms.assetid: 17eaf6b0-e2e1-4a23-952d-2439da89f765
ms.date: 12/05/2018
ms.keywords: AddRefresher, AddRefresher method [Windows Management Instrumentation], AddRefresher method [Windows Management Instrumentation],IWbemConfigureRefresher interface, IWbemConfigureRefresher interface [Windows Management Instrumentation],AddRefresher method, IWbemConfigureRefresher.AddRefresher, IWbemConfigureRefresher::AddRefresher, _hmm_iwbemconfigurerefresher_addrefresher, wbemcli/IWbemConfigureRefresher::AddRefresher, wmi.iwbemconfigurerefresher_addrefresher
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
 - IWbemConfigureRefresher::AddRefresher
 - wbemcli/IWbemConfigureRefresher::AddRefresher
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
 - IWbemConfigureRefresher.AddRefresher
---

# IWbemConfigureRefresher::AddRefresher


## -description

The 
<b>IWbemConfigureRefresher::AddRefresher</b> method adds a refresher to a refresher. The newly added refresher is called a "child refresher" or "nested refresher". You can use this method to create a single refresher containing more than one refresher that can be updated using a single call to the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">Refresh</a> method.

## -parameters

### -param pRefresher [in]

Pointer to a 
<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a> object to nest in this refresher.

### -param lFlags

Reserved. This parameter must be 0 (zero).

### -param plId [out]

Pointer to an integer returned by the provider that uniquely identifies the refreshable object.

## -returns

This method returns an <b>HRESULT</b> indicating the status of the method call. The following list lists the value contained within an <b>HRESULT</b>.

## -remarks

Users should not add recursively nested refreshers. The returned identifier can be used by the 
<a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-remove">Remove</a> function to remove the refresher. Although it is not necessary for the client to explicitly remove added refreshers, the client must call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> on the refreshers when they are no longer required.

## -see-also

<a href="/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="/windows/desktop/api/wbemcli/nn-wbemcli-iwbemconfigurerefresher">IWbemConfigureRefresher</a>



<a href="/windows/desktop/WmiSdk/making-an-instance-provider-into-a-high-performance-provider">Making an Instance Provider into a High-Performance Provider</a>



<a href="/windows/desktop/WmiSdk/performance-counter-provider">Performance Counter Provider</a>