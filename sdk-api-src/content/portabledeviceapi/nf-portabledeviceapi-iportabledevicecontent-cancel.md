---
UID: NF:portabledeviceapi.IPortableDeviceContent.Cancel
title: IPortableDeviceContent::Cancel (portabledeviceapi.h)
description: The Cancel method cancels a pending operation called on this interface.
helpviewer_keywords: ["Cancel","Cancel method [Windows Portable Devices SDK]","Cancel method [Windows Portable Devices SDK]","IPortableDeviceContent interface","IPortableDeviceContent interface [Windows Portable Devices SDK]","Cancel method","IPortableDeviceContent.Cancel","IPortableDeviceContent::Cancel","IPortableDeviceContentCancel","portabledeviceapi/IPortableDeviceContent::Cancel","wpdsdk.iportabledevicecontent_cancel"]
old-location: wpdsdk\iportabledevicecontent_cancel.htm
tech.root: wpdsdk
ms.assetid: adc63916-5d41-4772-9c78-72fdd8dcf1a8
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceContent.Cancel, IPortableDeviceContent::Cancel, IPortableDeviceContentCancel, portabledeviceapi/IPortableDeviceContent::Cancel, wpdsdk.iportabledevicecontent_cancel
f1_keywords:
- portabledeviceapi/IPortableDeviceContent.Cancel
dev_langs:
- c++
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
- IPortableDeviceContent.Cancel
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDeviceContent::Cancel


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



This method cancels all pending operations on the current device handle, which corresponds to a session associated with an <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice</a> interface. The Windows Portable Devices (WPD) API does not support targeted cancellation of specific operations.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>
 

 

