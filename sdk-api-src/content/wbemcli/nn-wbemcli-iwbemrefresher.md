---
UID: NN:wbemcli.IWbemRefresher
title: IWbemRefresher
author: windows-sdk-content
description: Provides an entry point through which refreshable objects such as enumerators or refresher objects, can be refreshed.
old-location: wmi\iwbemrefresher.htm
tech.root: WmiSdk
ms.assetid: cd1d652a-f0ce-401c-9a5e-074e6bb4d9ed
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWbemRefresher, IWbemRefresher interface [Windows Management Instrumentation], IWbemRefresher interface [Windows Management Instrumentation],described, WbemRefresher, _hmm_iwbemrefresher, wbemcli/IWbemRefresher, wmi.iwbemrefresher
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IWbemRefresher
 - WbemRefresher
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemRefresher interface


## -description


The 
<b>IWbemRefresher</b> interface provides an entry point through which refreshable objects such as enumerators or refresher objects, can be refreshed. Implementers of 
<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a> must provide an implementation of this interface.

WMI supplies a client implementation of this interface. Clients can access this interface by calling <a href="https://msdn.microsoft.com/en-us/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> on <b>CLSID_WbemRefresher</b>. This is the only supported implementation on the client.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemRefresher</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemRefresher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemRefresher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">Refresh</a>
</td>
<td align="left" width="63%">
Updates information in this refresher.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/5fa8f1b5-fd19-4d45-9b53-bc7089eecdb1">COM API for WMI</a>



<a href="https://msdn.microsoft.com/a4f537ba-9081-43b4-acff-4d206de3d9d7">Developing a WMI Provider</a>



<a href="https://msdn.microsoft.com/9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43">IWbemConfigureRefresher</a>



<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Making an Instance Provider into a High-Performance Provider</a>



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>



<a href="https://msdn.microsoft.com/d53c3399-cba8-4b5d-8da0-b5a23f94c0ae">Writing an Instance Provider</a>
 

 

