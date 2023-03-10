---
UID: NF:portabledeviceapi.IPortableDeviceDispatchFactory.GetDeviceDispatch
title: IPortableDeviceDispatchFactory::GetDeviceDispatch (portabledeviceapi.h)
description: Instantiates a WPD Automation Device object for a given WPD device identifier. (IPortableDeviceDispatchFactory.GetDeviceDispatch)
helpviewer_keywords: ["GetDeviceDispatch","GetDeviceDispatch method [WPD Automation]","GetDeviceDispatch method [WPD Automation]","IPortableDeviceDispatchFactory interface","IPortableDeviceDispatchFactory interface [WPD Automation]","GetDeviceDispatch method","IPortableDeviceDispatchFactory.GetDeviceDispatch","IPortableDeviceDispatchFactory::GetDeviceDispatch","portabledeviceapi/IPortableDeviceDispatchFactory::GetDeviceDispatch","wpdauto.iportabledevicedispatchfactory_getdevicedispatch"]
old-location: wpdauto\iportabledevicedispatchfactory_getdevicedispatch.htm
tech.root: wpdauto
ms.assetid: 80aa36cd-3831-4eb5-a5bb-a8e48f20fc62
ms.date: 12/05/2018
ms.keywords: GetDeviceDispatch, GetDeviceDispatch method [WPD Automation], GetDeviceDispatch method [WPD Automation],IPortableDeviceDispatchFactory interface, IPortableDeviceDispatchFactory interface [WPD Automation],GetDeviceDispatch method, IPortableDeviceDispatchFactory.GetDeviceDispatch, IPortableDeviceDispatchFactory::GetDeviceDispatch, portabledeviceapi/IPortableDeviceDispatchFactory::GetDeviceDispatch, wpdauto.iportabledevicedispatchfactory_getdevicedispatch
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceDispatchFactory::GetDeviceDispatch
 - portabledeviceapi/IPortableDeviceDispatchFactory::GetDeviceDispatch
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGuids.lib
 - PortableDeviceGuids.dll
api_name:
 - IPortableDeviceDispatchFactory.GetDeviceDispatch
---

# IPortableDeviceDispatchFactory::GetDeviceDispatch


## -description

Instantiates a WPD Automation <a href="/previous-versions/windows/desktop/wiaaut/-wiaaut-device">Device</a> object for a given WPD device identifier.

## -parameters

### -param pszPnPDeviceID [in]

A pointer to a <b>String</b> that is used by Plug-and-play to identify a currently connected WPD device. The Plug and Play (PnP) identifier for a particular device can be obtained from the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicemanager-getdevices">IPortableDeviceManager::GetDevices</a> method in the WPD C++/COM API.

### -param ppDeviceDispatch [out]

Contains a pointer to the <b>IDispatch</b> implementation for the WPD Automation <a href="/previous-versions/windows/desktop/wiaaut/-wiaaut-device">Device</a> object.

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
  <a href="/previous-versions/windows/desktop/wpdauto/instantiating-the-wpd-automation-factory-interface">Instantiating the WPD Automation Factory Interface</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/dd389207(v=vs.85)">Device Object</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicedispatchfactory">IPortableDeviceDispatchFactory Interface</a>



<a href="/previous-versions/windows/desktop/wpdauto/instantiating-the-wpd-automation-factory-interface">Instantiating the WPD Automation Factory Interface</a>
