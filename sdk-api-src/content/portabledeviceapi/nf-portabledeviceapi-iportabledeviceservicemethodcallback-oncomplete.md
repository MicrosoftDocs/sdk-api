---
UID: NF:portabledeviceapi.IPortableDeviceServiceMethodCallback.OnComplete
title: IPortableDeviceServiceMethodCallback::OnComplete
author: windows-driver-content
description: Indicates that a callback method has completed execution.
old-location: wpdsdk\iportabledeviceservicemethodcallback_oncomplete.htm
old-project: wpd_sdk
ms.assetid: b04e7bf1-bad7-4e9a-b53a-ec064d323f94
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: IPortableDeviceServiceMethodCallback interface [Windows Portable Devices SDK],OnComplete method, IPortableDeviceServiceMethodCallback.OnComplete, IPortableDeviceServiceMethodCallback::OnComplete, OnComplete, OnComplete method [Windows Portable Devices SDK], OnComplete method [Windows Portable Devices SDK],IPortableDeviceServiceMethodCallback interface, portabledeviceapi/IPortableDeviceServiceMethodCallback::OnComplete, wpdsdk.iportabledeviceservicemethodcallback_oncomplete
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
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
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceAPI.h
api_name:
-	IPortableDeviceServiceMethodCallback.OnComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDeviceServiceMethodCallback::OnComplete


## -description


The <b>OnComplete</b> method indicates that a callback method has completed execution.


## -parameters




### -param hrStatus [in]

The overall status of the method.


### -param pResults [in]

An <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that contains the method-execution results.  This is empty if the method returns no results.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -see-also




<a href="https://msdn.microsoft.com/cda7e4f7-0006-4b87-ac68-d07004440ce8">IPortableDeviceServiceMethodCallback Interface</a>
 

 

