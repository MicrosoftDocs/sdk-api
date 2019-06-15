---
UID: NN:wbemcli.IWbemHiPerfEnum
title: IWbemHiPerfEnum (wbemcli.h)
author: windows-sdk-content
description: Used in refresher operations to provide rapid access to enumerations of instance objects.
old-location: wmi\iwbemhiperfenum.htm
tech.root: WmiSdk
ms.assetid: 71ce1c89-446e-4137-9857-9d3c5921e0b7
ms.author: windowssdkdev
ms.date: 12/05/2018
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
ms.custom: 19H1
---

# IWbemHiPerfEnum interface


## -description


The 
<b>IWbemHiPerfEnum</b> interface is used in refresher operations to provide rapid access to enumerations of instance objects. WMI provides an implementation of this interface, which it passes to providers when 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemprov/nf-wbemprov-iwbemhiperfprovider-createrefreshableenum">IWbemHiPerfProvider::CreateRefreshableEnum</a> is called, and it returns to clients when 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemconfigurerefresher-addenum">IWbemConfigureRefresher::AddEnum</a> is called.

Client applications can call only the 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects">GetObjects</a> method of this interface. Attempts by client applications to call the other 
<b>IWbemHiPerfEnum</b> methods return WBEM_E_ACCESS_DENIED. Providers call these other methods to update the enumerators whenever a client calls 
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemrefresher-refresh">Refresh</a>.
<div class="alert"><b>Note</b>  This interface is not implemented by the user or by a provider under any circumstances. The implementation provided by WMI is the only one supported.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemHiPerfEnum</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IWbemHiPerfEnum</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemhiperfenum-addobjects">AddObjects</a>
</td>
<td align="left" width="63%">
Adds objects with assigned identifiers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemhiperfenum-getobjects">GetObjects</a>
</td>
<td align="left" width="63%">
Retrieves objects from the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemhiperfenum-removeall">RemoveAll</a>
</td>
<td align="left" width="63%">
Removes all objects from the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbemhiperfenum-removeobjects">RemoveObjects</a>
</td>
<td align="left" width="63%">
Remove objects with the specified identifiers.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/accessing-performance-data-in-c--">Accessing Performance Data in C++</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/accessing-wmi-preinstalled-performance-classes">Accessing WMI Preinstalled Performance Classes</a>



<a href="https://docs.microsoft.com/windows/desktop/WmiSdk/com-api-for-wmi">COM API for WMI</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nn-wbemcli-iwbemrefresher">IWbemRefresher</a>
 

 

