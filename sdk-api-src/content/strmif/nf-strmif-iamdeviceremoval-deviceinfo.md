---
UID: NF:strmif.IAMDeviceRemoval.DeviceInfo
title: IAMDeviceRemoval::DeviceInfo
author: windows-sdk-content
description: The DeviceInfo method retrieves information about the device.
old-location: dshow\iamdeviceremoval_deviceinfo.htm
old-project: DirectShow
ms.assetid: ec3628cf-fcb4-46c4-9de1-79bf1259c3db
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DeviceInfo, DeviceInfo method [DirectShow], DeviceInfo method [DirectShow],IAMDeviceRemoval interface, IAMDeviceRemoval interface [DirectShow],DeviceInfo method, IAMDeviceRemoval.DeviceInfo, IAMDeviceRemoval::DeviceInfo, IAMDeviceRemovalDeviceInfo, dshow.iamdeviceremoval_deviceinfo, strmif/IAMDeviceRemoval::DeviceInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMDeviceRemoval.DeviceInfo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMDeviceRemoval::DeviceInfo


## -description



The <code>DeviceInfo</code> method retrieves information about the device.




## -parameters




### -param pclsidInterfaceClass [out]

Receives a GUID that specifies the device interface class.


### -param pwszSymbolicLink [out]

Receives a pointer to a string that contains the Plug and Play (PnP) device path for the device. The caller must release the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>. This parameter can be <b>NULL</b>.


## -returns



If the method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



For more information about the device interface classes and device paths, see Device I/O in the Windows SDK documentation.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/3d67f577-9d85-47ca-b887-f259e9acc964">IAMDeviceRemoval Interface</a>
 

 

