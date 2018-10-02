---
UID: NN:wbemcli.IWbemConfigureRefresher
title: IWbemConfigureRefresher
author: windows-sdk-content
description: The IWbemConfigureRefresher interface is used by client code to add enumerators, objects, and nested refreshers into a refresher.
old-location: wmi\iwbemconfigurerefresher.htm
tech.root: WmiSdk
ms.assetid: 9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: IWbemConfigureRefresher, IWbemConfigureRefresher interface [Windows Management Instrumentation], IWbemConfigureRefresher interface [Windows Management Instrumentation],described, _hmm_iwbemconfigurerefresher, wbemcli/IWbemConfigureRefresher, wmi.iwbemconfigurerefresher
ms.prod: windows
ms.technology: windows-sdk
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
 - IWbemConfigureRefresher
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWbemConfigureRefresher interface


## -description


The 
<b>IWbemConfigureRefresher</b> interface is used by client code to add enumerators, objects, and nested refreshers into a refresher.

Users and providers should never implement this interface. The implementation provided by WMI is the only one that is supported.

By providing a native implementation of this interface, WMI allows client code to easily configure refreshers. You can access the 
<b>IWbemConfigureRefresher</b> interface by calling <a href="_com_iunknown_queryinterface">QueryInterface</a> on <b>IID_IWbemConfigureRefresher</b> on the object returned by calling <a href="_com_cocreateinstance">CoCreateInstance</a> on <b>CLSID_WbemRefresher</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWbemConfigureRefresher</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWbemConfigureRefresher</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWbemConfigureRefresher</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5b013267-78bc-4372-b55a-58e330acf927">AddEnum</a>
</td>
<td align="left" width="63%">
Adds an enumerator to a refresher.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85721e0c-863b-45af-91ca-8ee14af37181">AddObjectByPath</a>
</td>
<td align="left" width="63%">
Adds an object to a refresher based on a relative path.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c3f25484-7c6c-4625-9d26-1c01d15b10c4">AddObjectByTemplate</a>
</td>
<td align="left" width="63%">
Adds an object to a refresher by specifying an 
<a href="https://msdn.microsoft.com/a3ce37d7-5580-4b84-9119-78412c8e0d27">IWbemClassObject</a> instance template.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/17eaf6b0-e2e1-4a23-952d-2439da89f765">AddRefresher</a>
</td>
<td align="left" width="63%">
Adds a refresher to a refresher.

Use this method to create a single refresher that contains more than one refresher, which can be updated using a single call to the 
<a href="https://msdn.microsoft.com/6de85040-c938-41dc-8240-0e21e89c7716">Refresh</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f6e68b95-e9d1-473e-add4-823b6db51709">Remove</a>
</td>
<td align="left" width="63%">
Removes an object, enumerator, or nested refresher from a refresher.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ee0a2ead-f53a-4651-a287-04a62eba3f84">Accessing Performance Data in C++</a>



<a href="https://msdn.microsoft.com/9dd56891-5f2f-4b0e-9f70-fd75cb9bbd43">IWbemConfigureRefresher</a>



<a href="https://msdn.microsoft.com/eb0d12c0-d746-4bae-b47d-50350d33447a">IWbemHiPerfProvider</a>



<a href="https://msdn.microsoft.com/6a22d6f7-d9e2-45fa-876d-921a4bc4f574">Making an Instance Provider into a High-Performance Provider</a>



<a href="https://msdn.microsoft.com/2c7206e7-f5f8-4d40-b993-56122e48069b">Performance Counter Provider</a>
 

 

