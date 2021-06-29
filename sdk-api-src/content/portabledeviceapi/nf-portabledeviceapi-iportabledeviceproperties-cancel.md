---
UID: NF:portabledeviceapi.IPortableDeviceProperties.Cancel
title: IPortableDeviceProperties::Cancel (portabledeviceapi.h)
description: The Cancel method cancels a pending call.
helpviewer_keywords: ["Cancel","Cancel method [Windows Portable Devices SDK]","Cancel method [Windows Portable Devices SDK]","IPortableDeviceProperties interface","IPortableDeviceProperties interface [Windows Portable Devices SDK]","Cancel method","IPortableDeviceProperties.Cancel","IPortableDeviceProperties::Cancel","IPortableDevicePropertiesCancel","portabledeviceapi/IPortableDeviceProperties::Cancel","wpdsdk.iportabledeviceproperties_cancel"]
old-location: wpdsdk\iportabledeviceproperties_cancel.htm
tech.root: wpdsdk
ms.assetid: 6443e742-1296-4be4-b426-1f277406c01c
ms.date: 12/05/2018
ms.keywords: Cancel, Cancel method [Windows Portable Devices SDK], Cancel method [Windows Portable Devices SDK],IPortableDeviceProperties interface, IPortableDeviceProperties interface [Windows Portable Devices SDK],Cancel method, IPortableDeviceProperties.Cancel, IPortableDeviceProperties::Cancel, IPortableDevicePropertiesCancel, portabledeviceapi/IPortableDeviceProperties::Cancel, wpdsdk.iportabledeviceproperties_cancel
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
 - IPortableDeviceProperties::Cancel
 - portabledeviceapi/IPortableDeviceProperties::Cancel
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
 - IPortableDeviceProperties.Cancel
---

# IPortableDeviceProperties::Cancel


## -description

The <b>Cancel</b> method cancels a pending call.



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

This method cancels all pending operations on the current device handle, which corresponds to a session associated with an <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevice">IPortableDevice</a> interface. The Windows Portable Devices (WPD) API does not support targeted cancellation of specific operations.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties">IPortableDeviceProperties Interface</a>
