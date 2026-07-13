---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.Cancel
title: IPortableDeviceServiceCapabilities::Cancel (portabledeviceapi.h)
description: Cancels a pending operation.
helpviewer_keywords: ["Cancel","Cancel method [Windows Portable Devices SDK]","Cancel method [Windows Portable Devices SDK]","IPortableDeviceServiceCapabilities interface","IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK]","Cancel method","IPortableDeviceServiceCapabilities.Cancel","IPortableDeviceServiceCapabilities::Cancel","portabledeviceapi/IPortableDeviceServiceCapabilities::Cancel","wpdsdk.iportabledeviceservicecapabilities_cancel"]
old-location: wpdsdk\iportabledeviceservicecapabilities_cancel.htm
tech.root: wpdsdk
ms.assetid: f83a23ab-88c4-4486-adad-2bdff6b34df9
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceServiceCapabilities.Cancel, IPortableDeviceServiceCapabilities::Cancel, portabledeviceapi/IPortableDeviceServiceCapabilities::Cancel, wpdsdk.iportabledeviceservicecapabilities_cancel
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
 - IPortableDeviceServiceCapabilities::Cancel
 - portabledeviceapi/IPortableDeviceServiceCapabilities::Cancel
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
 - IPortableDeviceServiceCapabilities.Cancel
---

# IPortableDeviceServiceCapabilities::Cancel


## -description

The <b>Cancel</b> method cancels a pending operation.



## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

This method cancels all pending operations on the current service handle, which corresponds to a session associated with an   <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservice">IPortableDeviceService</a>  interface. The Windows Portable Devices (WPD) API does not support targeted cancellation of specific operations.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicecapabilities">IPortableDeviceServiceCapabilities Interface</a>
