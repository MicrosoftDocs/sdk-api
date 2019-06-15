---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulk.Cancel
title: IPortableDevicePropertiesBulk::Cancel (portabledeviceapi.h)
author: windows-sdk-content
description: The Cancel method cancels a pending properties request.
old-location: wpdsdk\iportabledevicepropertiesbulk_cancel.htm
tech.root: wpd_sdk
ms.assetid: 18a3458d-df93-4bdf-b5f2-f0197c35a1dd
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDevicePropertiesBulk interface, IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],Cancel method, IPortableDevicePropertiesBulk.Cancel, IPortableDevicePropertiesBulk::Cancel, IPortableDevicePropertiesBulkCancel, portabledeviceapi/IPortableDevicePropertiesBulk::Cancel, wpdsdk.iportabledevicepropertiesbulk_cancel
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
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevicePropertiesBulk.Cancel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDevicePropertiesBulk::Cancel


## -description



The <b>Cancel</b> method cancels a pending properties request.




## -parameters




### -param pContext [in]

Pointer to a context GUID that was retrieved when an asynchronous request was started by calling one of the <b>Queue...</b> methods.


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
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk Interface</a>
 

 

