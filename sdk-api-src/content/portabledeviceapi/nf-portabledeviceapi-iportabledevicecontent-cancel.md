---
UID: NF:portabledeviceapi.IPortableDeviceContent.Cancel
title: IPortableDeviceContent::Cancel method
author: windows-driver-content
description: The Cancel method cancels a pending operation called on this interface.
old-location: wpdsdk\iportabledevicecontent_cancel.htm
old-project: wpd_sdk
ms.assetid: adc63916-5d41-4772-9c78-72fdd8dcf1a8
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK], IPortableDeviceContent interface, Cancel,IPortableDeviceContent.Cancel, IPortableDeviceContent, IPortableDeviceContent interface [Windows Portable Devices SDK], Cancel method, IPortableDeviceContent::Cancel, IPortableDeviceContentCancel, portabledeviceapi/IPortableDeviceContent::Cancel, wpdsdk.iportabledevicecontent_cancel
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
req.typenames: WPD_WHITE_BALANCE_SETTINGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDeviceContent.Cancel
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IPortableDeviceContent::Cancel method


## -description



        The <b>Cancel</b> method cancels a pending operation called on this interface.
      




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




<a href="https://msdn.microsoft.com/7a03c673-8e7f-41a4-81ba-88406af2762d">IPortableDeviceContent Interface</a>
 

 

