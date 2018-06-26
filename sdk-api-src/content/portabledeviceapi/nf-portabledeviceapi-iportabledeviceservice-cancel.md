---
UID: NF:portabledeviceapi.IPortableDeviceService.Cancel
title: IPortableDeviceService::Cancel
author: windows-sdk-content
description: Cancels a pending operation on this interface.
old-location: wpdsdk\iportabledeviceservice_cancel.htm
old-project: wpd_sdk
ms.assetid: 1fb07c56-4e7a-4c20-8e1e-65d8a2c719ab
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceService interface, IPortableDeviceService interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceService.Cancel, IPortableDeviceService::Cancel, portabledeviceapi/IPortableDeviceService::Cancel, wpdsdk.iportabledeviceservice_cancel
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
 - IPortableDeviceService.Cancel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceService::Cancel


## -description


The <b>Cancel</b> method cancels a pending operation on this interface.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



This method cancels all pending operations on the current device handle, which corresponds to a session associated with an <a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService</a> interface. The Windows Portable Devices (WPD) API does not support targeted cancellation of specific operations.

If your application invokes the WPD API from multiple threads, each thread should create a new instance of the <a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService</a> interface. Doing this ensures that any cancel operation affects only the I/O for the affected thread. 




## -see-also




<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>
 

 

