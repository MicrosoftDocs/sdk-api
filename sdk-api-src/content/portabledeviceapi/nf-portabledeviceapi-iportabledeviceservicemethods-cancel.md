---
UID: NF:portabledeviceapi.IPortableDeviceServiceMethods.Cancel
title: IPortableDeviceServiceMethods::Cancel
author: windows-sdk-content
description: Cancels a pending method invocation.
old-location: wpdsdk\iportabledeviceservicemethods_cancel.htm
old-project: wpd_sdk
ms.assetid: 03281c4f-4dba-4ac4-af5d-d700c914ed01
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceServiceMethods interface, IPortableDeviceServiceMethods interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceServiceMethods.Cancel, IPortableDeviceServiceMethods::Cancel, portabledeviceapi/IPortableDeviceServiceMethods::Cancel, wpdsdk.iportabledeviceservicemethods_cancel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceServiceMethods.Cancel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
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



A callback object identifies a method invocation. If the same callback object is reused for multiple calls to the <a href="https://msdn.microsoft.com/0acf416c-4d59-4eb5-b1ce-aef848b54949">InvokeAsync</a> method, all method invocations arising from these calls will be cancelled.

To enable targeted cancellation of a specific method invocation, pass a unique instance of the <a href="https://msdn.microsoft.com/cda7e4f7-0006-4b87-ac68-d07004440ce8">IPortableDeviceServiceMethodCallback</a> interface to the <a href="https://msdn.microsoft.com/0acf416c-4d59-4eb5-b1ce-aef848b54949">InvokeAsync</a> method.
  
  




## -see-also




<a href="https://msdn.microsoft.com/9d233dea-91b6-4358-830c-6abe466264e5">IPortableDeviceServiceMethods Interface</a>
 

 

