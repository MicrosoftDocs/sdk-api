---
UID: NF:portabledeviceapi.IPortableDeviceServiceMethods.Cancel
title: IPortableDeviceServiceMethods::Cancel (portabledeviceapi.h)
description: Cancels a pending method invocation.
helpviewer_keywords: ["Cancel","Cancel method [Windows Portable Devices SDK]","Cancel method [Windows Portable Devices SDK]","IPortableDeviceServiceMethods interface","IPortableDeviceServiceMethods interface [Windows Portable Devices SDK]","Cancel method","IPortableDeviceServiceMethods.Cancel","IPortableDeviceServiceMethods::Cancel","portabledeviceapi/IPortableDeviceServiceMethods::Cancel","wpdsdk.iportabledeviceservicemethods_cancel"]
old-location: wpdsdk\iportabledeviceservicemethods_cancel.htm
tech.root: wpdsdk
ms.assetid: 03281c4f-4dba-4ac4-af5d-d700c914ed01
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceServiceMethods interface, IPortableDeviceServiceMethods interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceServiceMethods.Cancel, IPortableDeviceServiceMethods::Cancel, portabledeviceapi/IPortableDeviceServiceMethods::Cancel, wpdsdk.iportabledeviceservicemethods_cancel
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
 - IPortableDeviceServiceMethods::Cancel
 - portabledeviceapi/IPortableDeviceServiceMethods::Cancel
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
 - IPortableDeviceServiceMethods.Cancel
---

# IPortableDeviceServiceMethods::Cancel


## -description

The <b>Cancel</b> method cancels a pending method invocation.

## -parameters

### -param pCallback [in]

A pointer to the callback object whose method invocation is to be canceled, or <b>NULL</b> to cancel all pending method invocations.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

A callback object identifies a method invocation. If the same callback object is reused for multiple calls to the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync">InvokeAsync</a> method, all method invocations arising from these calls will be cancelled.

To enable targeted cancellation of a specific method invocation, pass a unique instance of the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback">IPortableDeviceServiceMethodCallback</a> interface to the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync">InvokeAsync</a> method.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethods">IPortableDeviceServiceMethods Interface</a>