---
UID: NN:portabledeviceapi.IPortableDeviceDispatchFactory
title: IPortableDeviceDispatchFactory
author: windows-sdk-content
description: Represents a factory that can instantiate a WPD Automation Device object.
old-location: wpdauto\iportabledevicedispatchfactory_interface.htm
tech.root: wpdauto
ms.assetid: 537551c9-0773-44a9-b602-7d2a6bf9ad00
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPortableDeviceDispatchFactory, IPortableDeviceDispatchFactory interface [WPD Automation], IPortableDeviceDispatchFactory interface [WPD Automation],described, portabledeviceapi/IPortableDeviceDispatchFactory, wpdauto.iportabledevicedispatchfactory_interface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGuids.lib
 - PortableDeviceGuids.dll
api_name:
 - IPortableDeviceDispatchFactory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceDispatchFactory interface


## -description


Represents a factory that can instantiate a WPD Automation <a href="https://msdn.microsoft.com/en-us/library/ms630493(v=VS.85).aspx">Device</a> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IPortableDeviceDispatchFactory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IPortableDeviceDispatchFactory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IPortableDeviceDispatchFactory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80aa36cd-3831-4eb5-a5bb-a8e48f20fc62">GetDeviceDispatch</a>
</td>
<td align="left" width="63%">
Instantiates a WPD Automation <a href="https://msdn.microsoft.com/en-us/library/ms630493(v=VS.85).aspx">Device</a> object for a given WPD device identifier.

</td>
</tr>
</table> 


## -remarks



The <b>IPortableDeviceDispatchFactory</b> interface can be CoCreated directly using <b>CLSID_PortableDeviceDispatchFactory</b> as in the following code.


```cpp
IPortableDeviceDispatchFactgory* pDeviceDispatchFactory = NULL;
HRESULT hr = CoCreateInstance(CLSID_PortableDeviceDispatchFactory, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pDeviceDispatchFactory));   

```



#### Examples

For an example of how to use the <b>IPortableDeviceDispatchFactory</b> interface to instantiate a WPD Automation <b>Device</b>  object, see 
  <a href="https://msdn.microsoft.com/d83db1cd-7bd2-42f1-b1f2-55090a332e9a">Instantiating the WPD Automation Factory Interface</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/012e266d-e1b0-4d15-841f-04b6d21d27ae">Device Object</a>



<a href="https://msdn.microsoft.com/d83db1cd-7bd2-42f1-b1f2-55090a332e9a">Instantiating the WPD Automation Factory Interface</a>



<a href="https://msdn.microsoft.com/c9fa92ab-8e6e-4b17-882c-83fcc0ac5c70">WPD Automation Reference</a>
 

 

