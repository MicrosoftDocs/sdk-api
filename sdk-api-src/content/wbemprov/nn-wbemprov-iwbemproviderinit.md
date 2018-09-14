---
UID: NN:wbemprov.IWbemProviderInit
title: IWbemProviderInit
author: windows-sdk-content
description: The IWbemProviderInit interface is called by Windows Management to initialize providers. All providers are required to implement IWbemProviderInit.
old-location: wmi\iwbemproviderinit.htm
tech.root: WmiSdk
ms.assetid: 92edf347-c694-4023-b83f-09531072c631
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: IWbemProviderInit, IWbemProviderInit interface [Windows Management Instrumentation], IWbemProviderInit interface [Windows Management Instrumentation],described, _hmm_iwbemproviderinit, wbemprov/IWbemProviderInit, wmi.iwbemproviderinit
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IWbemProviderInit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemProviderInit interface


## -description


The 
<b>IWbemProviderInit</b> interface is called by Windows Management to initialize providers. All providers are required to implement 
<b>IWbemProviderInit</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemProviderInit</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemProviderInit</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemProviderInit</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/437d803d-b916-4209-bbf0-64b1ec3b7068">Initialize</a>
</td>
<td align="left" width="63%">
Called by Windows Management to initialize a provider.

</td>
</tr>
</table> 

