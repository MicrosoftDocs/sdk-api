---
UID: NF:portabledeviceapi.IPortableDeviceServiceManager.GetDeviceForService
title: IPortableDeviceServiceManager::GetDeviceForService
author: windows-sdk-content
description: Retrieves the device associated with the specified service.
old-location: wpdsdk\iportabledeviceservicemanager_getdeviceforservice.htm
tech.root: wpd_sdk
ms.assetid: 2cdb03fb-8cb2-4eee-af90-3aec0a055fc5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetDeviceForService, GetDeviceForService method [Windows Portable Devices SDK], GetDeviceForService method [Windows Portable Devices SDK],IPortableDeviceServiceManager interface, IPortableDeviceServiceManager interface [Windows Portable Devices SDK],GetDeviceForService method, IPortableDeviceServiceManager.GetDeviceForService, IPortableDeviceServiceManager::GetDeviceForService, portabledeviceapi/IPortableDeviceServiceManager::GetDeviceForService, wpdsdk.iportabledeviceservicemanager_getdeviceforservice
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceManager.GetDeviceForService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceServiceManager::GetDeviceForService


## -description


The <b>GetDeviceForService</b> method retrieves the device associated with the specified service.


## -parameters




### -param pszPnPServiceID [in]

The Plug and Play (PnP) identifier of the service.


### -param ppszPnPDeviceID [out]

The retrieved PnP identifier of the device associated with the service.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
An invalid pointer was supplied.

</td>
</tr>
</table>
 




## -remarks



Neither the <i>pszPnPServiceID</i> parameter nor the <i>pszPnPDeviceID</i> parameter can be <b>NULL</b>.

An application can retrieve a PnP service identifier by calling the <b>GetDeviceServices</b> method.




## -see-also




<a href="https://msdn.microsoft.com/8df23343-26f0-4fb0-90b9-e8b75bcadffa">IPortableDeviceServiceManager Interface</a>
 

 

