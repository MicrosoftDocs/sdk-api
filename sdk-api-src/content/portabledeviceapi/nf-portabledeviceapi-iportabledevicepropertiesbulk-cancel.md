---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulk.Cancel
title: IPortableDevicePropertiesBulk::Cancel
author: windows-sdk-content
description: The Cancel method cancels a pending properties request.
old-location: wpdsdk\iportabledevicepropertiesbulk_cancel.htm
old-project: wpd_sdk
ms.assetid: 18a3458d-df93-4bdf-b5f2-f0197c35a1dd
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDevicePropertiesBulk interface, IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],Cancel method, IPortableDevicePropertiesBulk.Cancel, IPortableDevicePropertiesBulk::Cancel, IPortableDevicePropertiesBulkCancel, portabledeviceapi/IPortableDevicePropertiesBulk::Cancel, wpdsdk.iportabledevicepropertiesbulk_cancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: portabledeviceapi.h
req.include-header: 
req.redist: 
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
 - IPortableDevicePropertiesBulk.Cancel
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: ADAM
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




<a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk Interface</a>
 

 

