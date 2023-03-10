---
UID: NF:portabledeviceapi.IPortableDeviceManager.RefreshDeviceList
title: IPortableDeviceManager::RefreshDeviceList (portabledeviceapi.h)
description: The RefreshDeviceList method refreshes the list of devices that are connected to the computer.
helpviewer_keywords: ["IPortableDeviceManager interface [Windows Portable Devices SDK]","RefreshDeviceList method","IPortableDeviceManager.RefreshDeviceList","IPortableDeviceManager::RefreshDeviceList","IPortableDeviceManagerRefreshDeviceList","RefreshDeviceList","RefreshDeviceList method [Windows Portable Devices SDK]","RefreshDeviceList method [Windows Portable Devices SDK]","IPortableDeviceManager interface","portabledeviceapi/IPortableDeviceManager::RefreshDeviceList","wpdsdk.iportabledevicemanager_refreshdevicelist"]
old-location: wpdsdk\iportabledevicemanager_refreshdevicelist.htm
tech.root: wpdsdk
ms.assetid: 89163407-7b38-4c79-8171-67a5b7e1d17c
ms.date: 12/05/2018
ms.keywords: IPortableDeviceManager interface [Windows Portable Devices SDK],RefreshDeviceList method, IPortableDeviceManager.RefreshDeviceList, IPortableDeviceManager::RefreshDeviceList, IPortableDeviceManagerRefreshDeviceList, RefreshDeviceList, RefreshDeviceList method [Windows Portable Devices SDK], RefreshDeviceList method [Windows Portable Devices SDK],IPortableDeviceManager interface, portabledeviceapi/IPortableDeviceManager::RefreshDeviceList, wpdsdk.iportabledevicemanager_refreshdevicelist
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceManager::RefreshDeviceList
 - portabledeviceapi/IPortableDeviceManager::RefreshDeviceList
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceManager.RefreshDeviceList
---

# IPortableDeviceManager::RefreshDeviceList


## -description

The <b>RefreshDeviceList</b> method refreshes the list of devices that are connected to the computer.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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

When the <b>IPortableDeviceManager</b> interface is instantiated the first time, it generates a list of the devices that are connected. However, devices can connect and disconnect from the computer, making the original list obsolete. This method enables an application to refresh the list of connected devices.

This method is less resource-intensive than instantiating a new device manager to generate a new device list. However, it does require some resources; therefore, we recommend that you do not call this method arbitrarily. The best solution is to have the application register to get device arrival and removal notifications, and when a notification is received, have the application call this function.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicemanager">IPortableDeviceManager Interface</a>
