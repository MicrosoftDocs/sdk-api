---
UID: NF:portabledeviceapi.IPortableDevice.Cancel
title: IPortableDevice::Cancel (portabledeviceapi.h)
description: The Cancel method cancels a pending operation on this interface.
helpviewer_keywords: ["Cancel","Cancel method [Windows Portable Devices SDK]","Cancel method [Windows Portable Devices SDK]","IPortableDevice interface","IPortableDevice interface [Windows Portable Devices SDK]","Cancel method","IPortableDevice.Cancel","IPortableDevice::Cancel","IPortableDeviceCancel","portabledeviceapi/IPortableDevice::Cancel","wpdsdk.iportabledevice_cancel"]
old-location: wpdsdk\iportabledevice_cancel.htm
tech.root: wpdsdk
ms.assetid: dcda2e43-ee12-44a4-a7ab-a2a542082d07
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDevice interface, IPortableDevice interface [Windows Portable Devices SDK],Cancel method, IPortableDevice.Cancel, IPortableDevice::Cancel, IPortableDeviceCancel, portabledeviceapi/IPortableDevice::Cancel, wpdsdk.iportabledevice_cancel
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDevice::Cancel
 - portabledeviceapi/IPortableDevice::Cancel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceGUIDs.lib
 - PortableDeviceGUIDs.dll
api_name:
 - IPortableDevice.Cancel
---

# IPortableDevice::Cancel


## -description

The <b>Cancel</b> method cancels a pending operation on this interface.



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
The operation was canceled successfully.

</td>
</tr>
</table>

## -remarks

If your application invokes the WPD API from multiple threads, each thread should create a new instance of the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice</a> interface. Doing this ensures that any cancel operation affects only the I/O for the affected thread.
      

If an <b>IStream</b> write operation is underway when the <b>Cancel</b> method is invoked, your application should discard all changes by invoking the <b>IStream::Revert</b> method. Once the changes are discarded, the application should also close the stream by invoking the <b>IUnknown::Release</b> method.

Also, note that if the <b>Cancel</b> method is invoked before an <b>IStream::Write</b> method has completed, the data being written may be corrupted.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice Interface</a>
