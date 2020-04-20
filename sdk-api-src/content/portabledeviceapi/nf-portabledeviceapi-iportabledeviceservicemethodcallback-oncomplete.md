---
UID: NF:portabledeviceapi.IPortableDeviceServiceMethodCallback.OnComplete
title: IPortableDeviceServiceMethodCallback::OnComplete (portabledeviceapi.h)
description: Indicates that a callback method has completed execution.helpviewer_keywords: ["IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK]","OnComplete method","IPortableDeviceServiceMethodCallback.OnComplete","IPortableDeviceServiceMethodCallback::OnComplete","OnComplete","OnComplete method [Windows Portable Devices SDK]","OnComplete method [Windows Portable Devices SDK]","IPortableDeviceServiceMethodCallback interface","portabledeviceapi/IPortableDeviceServiceMethodCallback::OnComplete","wpdsdk.iportabledeviceservicemethodcallback_oncomplete"]
old-location: wpdsdk\iportabledeviceservicemethodcallback_oncomplete.htm
tech.root: wpd_sdk
ms.assetid: b04e7bf1-bad7-4e9a-b53a-ec064d323f94
ms.date: 12/05/2018
ms.keywords: IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK],OnComplete method, IPortableDeviceServiceMethodCallback.OnComplete, IPortableDeviceServiceMethodCallback::OnComplete, OnComplete, OnComplete method [Windows Portable Devices SDK], OnComplete method [Windows Portable Devices SDK],IPortableDeviceServiceMethodCallback interface, portabledeviceapi/IPortableDeviceServiceMethodCallback::OnComplete, wpdsdk.iportabledeviceservicemethodcallback_oncomplete
f1_keywords:
- portabledeviceapi/IPortableDeviceServiceMethodCallback.OnComplete
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
- IPortableDeviceServiceMethodCallback.OnComplete
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceServiceMethodCallback::OnComplete


## -description


The <b>OnComplete</b> method indicates that a callback method has completed execution.


## -parameters




### -param hrStatus [in]

The overall status of the method.


### -param pResults [in]

An <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that contains the method-execution results.  This is empty if the method returns no results.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceservicemethodcallback">IPortableDeviceServiceMethodCallback Interface</a>
 

 

