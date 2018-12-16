---
UID: NN:wbemcli.IWbemHiPerfEnum
title: IWbemHiPerfEnum
author: windows-sdk-content
description: Used in refresher operations to provide rapid access to enumerations of instance objects.
old-location: wmi\iwbemhiperfenum.htm
tech.root: WmiSdk
ms.assetid: 71ce1c89-446e-4137-9857-9d3c5921e0b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWbemHiPerfEnum, IWbemHiPerfEnum interface [Windows Management Instrumentation], IWbemHiPerfEnum interface [Windows Management Instrumentation],described, _hmm_iwbemhiperfenum, wbemcli/IWbemHiPerfEnum, wmi.iwbemhiperfenum
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemHiPerfEnum interface


## -description


The 
<b>IWbemHiPerfEnum</b> interface is used in refresher operations to provide rapid access to enumerations of instance objects. WMI provides an implementation of this interface, which it passes to providers when 
<a href="https://msdn.microsoft.com/086a1717-b6e8-45c1-9397-ec894ee900a0">IWbemHiPerfProvider::CreateRefreshableEnum</a> is called, and it returns to clients when 
<a href="https://msdn.microsoft.com/5b013267-78bc-4372-b55a-58e330acf927">IWbemConfigureRefresher::AddEnum</a> is called.

Client applications can call only the 
<a href="https://msdn.microsoft.com/27dd9c2c-236e-41be-bfaa-90ebf8dfb1bc">GetObjects</a> method of this interface. Attempts by client applications to call the other 
<b>IWbemHiPerfEnum</b> methods return WBEM_E_ACCESS_DENIED. Providers call these other methods to update the enumerators whenever a client calls 
<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">Refresh</a>.
<div class="alert"><b>Note</b>  This interface is not implemented by the user or by a provider under any circumstances. The implementation provided by WMI is the only one supported.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemHiPerfEnum</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemHiPerfEnum</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemHiPerfEnum</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6a6cd0f9-c6ed-4c9c-aa0f-7af2ac0fe73a">AddObjects</a>
</td>
<td align="left" width="63%">
Adds objects with assigned identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/27dd9c2c-236e-41be-bfaa-90ebf8dfb1bc">GetObjects</a>
</td>
<td align="left" width="63%">
Retrieves objects from the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/51692902-0b92-4a25-b42b-3802be19eba5">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all objects from the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4f25be2-8450-4e4c-ba6a-8d78c1fefca1">RemoveObjects</a>
</td>
<td align="left" width="63%">
Remove objects with the specified identifiers.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/2158385f-d0dc-4102-84db-ce02d2b0ee53">Accessing WMI Preinstalled Performance Classes</a>



<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed">IWbemRefresher</a>
 

 

