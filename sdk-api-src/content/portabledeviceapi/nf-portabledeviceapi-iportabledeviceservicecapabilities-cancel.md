---
UID: NF:portabledeviceapi.IPortableDeviceServiceCapabilities.Cancel
title: IPortableDeviceServiceCapabilities::Cancel
author: windows-driver-content
description: Cancels a pending operation.
old-location: wpdsdk\iportabledeviceservicecapabilities_cancel.htm
old-project: wpd_sdk
ms.assetid: f83a23ab-88c4-4486-adad-2bdff6b34df9
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceServiceCapabilities interface, IPortableDeviceServiceCapabilities interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceServiceCapabilities.Cancel, IPortableDeviceServiceCapabilities::Cancel, portabledeviceapi/IPortableDeviceServiceCapabilities::Cancel, wpdsdk.iportabledeviceservicecapabilities_cancel
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
-	IPortableDeviceServiceCapabilities.Cancel
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDeviceServiceCapabilities::Cancel


## -description


The <b>Cancel</b> method cancels a pending operation.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



This method cancels all pending operations on the current service handle, which corresponds to a session associated with an   <a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService</a>  interface. The Windows Portable Devices (WPD) API does not support targeted cancellation of specific operations.




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

