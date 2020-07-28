---
UID: NN:wbemprov.IWbemProviderInitSink
title: IWbemProviderInitSink (wbemprov.h)
description: The IWbemProviderInitSink interface is implemented by WMI and called by providers to report initialization status.
helpviewer_keywords: ["IWbemProviderInitSink","IWbemProviderInitSink interface [Windows Management Instrumentation]","IWbemProviderInitSink interface [Windows Management Instrumentation]","described","_hmm_iwbemproviderinitsink","wbemprov/IWbemProviderInitSink","wmi.iwbemproviderinitsink"]
old-location: wmi\iwbemproviderinitsink.htm
tech.root: wmi
ms.assetid: abcee170-6a28-44d2-97d6-cb62c393b534
ms.date: 12/05/2018
ms.keywords: IWbemProviderInitSink, IWbemProviderInitSink interface [Windows Management Instrumentation], IWbemProviderInitSink interface [Windows Management Instrumentation],described, _hmm_iwbemproviderinitsink, wbemprov/IWbemProviderInitSink, wmi.iwbemproviderinitsink
f1_keywords:
- wbemprov/IWbemProviderInitSink
dev_langs:
- c++
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
req.dll: Wbemsvc.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wbemsvc.dll
api_name:
- IWbemProviderInitSink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWbemProviderInitSink interface


## -description


The 
<b>IWbemProviderInitSink</b> interface is implemented by WMI and called by providers to report initialization status.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemProviderInitSink</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemProviderInitSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemProviderInitSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemproviderinitsink-setstatus">SetStatus</a>
</td>
<td align="left" width="63%">
Called by the provider to indicate success or failure of initialization.

</td>
</tr>
</table> 

