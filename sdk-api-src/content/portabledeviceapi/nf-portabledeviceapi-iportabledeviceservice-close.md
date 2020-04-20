---
UID: NF:portabledeviceapi.IPortableDeviceService.Close
title: IPortableDeviceService::Close (portabledeviceapi.h)
description: Releases the connection to the service.helpviewer_keywords: ["Close","Close method [Windows Portable Devices SDK]","Close method [Windows Portable Devices SDK]","IPortableDeviceService interface","IPortableDeviceService interface [Windows Portable Devices SDK]","Close method","IPortableDeviceService.Close","IPortableDeviceService::Close","portabledeviceapi/IPortableDeviceService::Close","wpdsdk.iportabledeviceservice_close"]
old-location: wpdsdk\iportabledeviceservice_close.htm
tech.root: wpd_sdk
ms.assetid: 59cfe8d7-47ce-4d1a-a53a-30f398100aa7
ms.date: 12/05/2018
ms.keywords: Close, Close method [Windows Portable Devices SDK], Close method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],Close method, IPortableDeviceService.Close, IPortableDeviceService::Close, portabledeviceapi/IPortableDeviceService::Close, wpdsdk.iportabledeviceservice_close
f1_keywords:
- portabledeviceapi/IPortableDeviceService.Close
dev_langs:
- c++
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
- IPortableDeviceService.Close
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceService::Close


## -description


The <b>Close</b> method releases the connection to the service.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Applications typically won't call this method, as the Windows Portable Devices (WPD) API automatically calls it when the last reference to a service is removed.

When an application does call this method, the WPD API releases the service connection, so that any WPD objects attached to the service will return the <b>E_WPD_SERVICE_NOT_OPEN</b> error.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService Interface</a>
 

 

