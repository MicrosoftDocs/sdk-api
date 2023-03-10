---
UID: NF:portabledeviceapi.IPortableDeviceService.GetServiceObjectID
title: IPortableDeviceService::GetServiceObjectID (portabledeviceapi.h)
description: Retrieves an object identifier for the service. This object identifier can be used to access the properties of the service, for example.
helpviewer_keywords: ["GetServiceObjectID","GetServiceObjectID method [Windows Portable Devices SDK]","GetServiceObjectID method [Windows Portable Devices SDK]","IPortableDeviceService interface","IPortableDeviceService interface [Windows Portable Devices SDK]","GetServiceObjectID method","IPortableDeviceService.GetServiceObjectID","IPortableDeviceService::GetServiceObjectID","portabledeviceapi/IPortableDeviceService::GetServiceObjectID","wpdsdk.iportabledeviceservice_getserviceobjectid"]
old-location: wpdsdk\iportabledeviceservice_getserviceobjectid.htm
tech.root: wpdsdk
ms.assetid: f86907c4-5d8a-4659-ab57-3c235face8cf
ms.date: 12/05/2018
ms.keywords: GetServiceObjectID, GetServiceObjectID method [Windows Portable Devices SDK], GetServiceObjectID method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],GetServiceObjectID method, IPortableDeviceService.GetServiceObjectID, IPortableDeviceService::GetServiceObjectID, portabledeviceapi/IPortableDeviceService::GetServiceObjectID, wpdsdk.iportabledeviceservice_getserviceobjectid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceService::GetServiceObjectID
 - portabledeviceapi/IPortableDeviceService::GetServiceObjectID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceService.GetServiceObjectID
---

# IPortableDeviceService::GetServiceObjectID


## -description

The <b>GetServiceObjectID</b> method retrieves an object identifier for the service.  This object identifier can be used to access the properties of the service, for example.

## -parameters

### -param ppszServiceObjectID [out]

The retrieved service object identifier.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService Interface</a>