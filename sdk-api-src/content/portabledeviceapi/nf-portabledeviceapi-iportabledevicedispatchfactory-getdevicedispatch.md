---
UID: NF:portabledeviceapi.IPortableDeviceDispatchFactory.GetDeviceDispatch
title: IPortableDeviceDispatchFactory::GetDeviceDispatch
author: windows-sdk-content
description: Instantiates a WPD Automation Device object for a given WPD device identifier.
old-location: wpdauto\iportabledevicedispatchfactory_getdevicedispatch.htm
old-project: wpdauto
ms.assetid: 80aa36cd-3831-4eb5-a5bb-a8e48f20fc62
ms.author: windowssdkdev
ms.date: 04/05/2018
ms.keywords: GetDeviceDispatch, GetDeviceDispatch method [WPD Automation], GetDeviceDispatch method [WPD Automation],IPortableDeviceDispatchFactory interface, IPortableDeviceDispatchFactory interface [WPD Automation],GetDeviceDispatch method, IPortableDeviceDispatchFactory.GetDeviceDispatch, IPortableDeviceDispatchFactory::GetDeviceDispatch, portabledeviceapi/IPortableDeviceDispatchFactory::GetDeviceDispatch, wpdauto.iportabledevicedispatchfactory_getdevicedispatch
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGuids.lib
-	PortableDeviceGuids.dll
api_name:
-	IPortableDeviceDispatchFactory.GetDeviceDispatch
product: Windows
targetos: Windows
req.lib: PortableDeviceGuids.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceDispatchFactory::GetDeviceDispatch


## -description


Instantiates a WPD Automation <a href="wpdauto.device_object_script">Device</a> object for a given WPD device identifier.


## -parameters




### -param pszPnPDeviceID [in]

A pointer to a <b>String</b> that is used by Plug-and-play to identify a currently connected WPD device. The Plug and Play (PnP) identifier for a particular device can be obtained from the <a href="https://msdn.microsoft.com/5061b3c0-8b93-480d-b1c6-0a6b616a2c8d">IPortableDeviceManager::GetDevices</a> method in the WPD C++/COM API.


### -param ppDeviceDispatch [out]

Contains a pointer to the <b>IDispatch</b> implementation for the WPD Automation <a href="wpdauto.device_object_script">Device</a> object.



## -returns



The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.


</td>
</tr>
</table>
 




## -remarks



 For an example of how to use <b>GetDeviceDispatch</b> method to instantiate a WPD Automation <b>Device</b>  object, see 
  <a href="https://msdn.microsoft.com/d83db1cd-7bd2-42f1-b1f2-55090a332e9a">Instantiating the WPD Automation Factory Interface</a>.
      





## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597563">Device Object</a>



<a href="https://msdn.microsoft.com/537551c9-0773-44a9-b602-7d2a6bf9ad00">IPortableDeviceDispatchFactory Interface</a>



<a href="https://msdn.microsoft.com/d83db1cd-7bd2-42f1-b1f2-55090a332e9a">Instantiating the WPD Automation Factory Interface</a>
 

 

