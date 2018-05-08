---
UID: NF:portabledeviceapi.IPortableDeviceCapabilities.Cancel
title: IPortableDeviceCapabilities::Cancel
author: windows-driver-content
description: The Cancel method cancels a pending request on this interface.
old-location: wpdsdk\iportabledevicecapabilities_cancel.htm
old-project: wpd_sdk
ms.assetid: 5883f855-826c-405f-939f-b2d28548c931
ms.author: windowsdriverdev
ms.date: 4/11/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceCapabilities interface, IPortableDeviceCapabilities interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceCapabilities.Cancel, IPortableDeviceCapabilities::Cancel, IPortableDeviceCapabilitiesCancel, portabledeviceapi/IPortableDeviceCapabilities::Cancel, wpdsdk.iportabledevicecapabilities_cancel
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDeviceCapabilities.Cancel
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPortableDeviceCapabilities::Cancel


## -description



        The <b>Cancel</b> method cancels a pending request on this interface.
      


## -parameters






## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method cancels all pending operations on the current device handle, which corresponds to a session associated with an <a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice</a> interface. The Windows Portable Devices (WPD) API does not support targeted cancellation of specific operations.




## -see-also




<a href="https://msdn.microsoft.com/c292a509-f202-4136-bbf7-b4e82ef2b936">IPortableDeviceCapabilities Interface</a>
 

 

