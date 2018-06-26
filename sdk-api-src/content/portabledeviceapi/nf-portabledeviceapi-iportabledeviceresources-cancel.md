---
UID: NF:portabledeviceapi.IPortableDeviceResources.Cancel
title: IPortableDeviceResources::Cancel
author: windows-sdk-content
description: The Cancel method cancels a pending operation.
old-location: wpdsdk\iportabledeviceresources_cancel.htm
old-project: wpd_sdk
ms.assetid: 5b36f5bb-43b3-4f2d-87f4-4df842350586
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceResources interface, IPortableDeviceResources interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceResources.Cancel, IPortableDeviceResources::Cancel, IPortableDeviceResourcesCancel, portabledeviceapi/IPortableDeviceResources::Cancel, wpdsdk.iportabledeviceresources_cancel
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDeviceResources.Cancel
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
---

# IPortableDeviceResources::Cancel


## -description



The <b>Cancel</b> method cancels a pending operation.




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
The method succeeded

</td>
</tr>
</table>
 




## -remarks



This method cancels all pending operations on the current device handle, which corresponds to a session associated with an <a href="https://msdn.microsoft.com/98c48e56-56b8-4800-b52b-ac08f2abf27e">IPortableDevice</a> interface. The Windows Portable Devices (WPD) API does not support targeted cancellation of specific operations.




## -see-also




<a href="https://msdn.microsoft.com/fce2d6db-13f0-4c1d-ba55-16139c6acbb7">IPortableDeviceResources Interface</a>
 

 

