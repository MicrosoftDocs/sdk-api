---
UID: NF:portabledeviceapi.IPortableDeviceContent.Copy
title: IPortableDeviceContent::Copy (portabledeviceapi.h)
description: The Copy method copies objects from one location on a device to another.
helpviewer_keywords: ["Copy","Copy method [Windows Portable Devices SDK]","Copy method [Windows Portable Devices SDK]","IPortableDeviceContent interface","IPortableDeviceContent interface [Windows Portable Devices SDK]","Copy method","IPortableDeviceContent.Copy","IPortableDeviceContent::Copy","IPortableDeviceContentCopy","portabledeviceapi/IPortableDeviceContent::Copy","wpdsdk.iportabledevicecontent_copy"]
old-location: wpdsdk\iportabledevicecontent_copy.htm
tech.root: wpdsdk
ms.assetid: 46d6abad-457c-47d7-a83a-b5ba2b84b064
ms.date: 12/05/2018
ms.keywords: Copy, Copy method [Windows Portable Devices SDK], Copy method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],Copy method, IPortableDeviceContent.Copy, IPortableDeviceContent::Copy, IPortableDeviceContentCopy, portabledeviceapi/IPortableDeviceContent::Copy, wpdsdk.iportabledevicecontent_copy
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
 - IPortableDeviceContent::Copy
 - portabledeviceapi/IPortableDeviceContent::Copy
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
 - IPortableDeviceContent.Copy
---

# IPortableDeviceContent::Copy


## -description

The <b>Copy</b> method copies objects from one location on a device to another.

## -parameters

### -param pObjectIDs

A collection of object identifiers for the objects that this method will copy.

### -param pszDestinationFolderObjectID

An object identifier for the destination folder (or functional storage) into which this method will copy the specified objects.

### -param ppResults [out]

A collection of VT_ERROR values indicating the success or failure of copying a particular element. The first error value corresponds to the first object in the collection of object identifiers, the second to the second element, and so on. This argument can be <b>NULL</b>.

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
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The copy operation failed for at least one object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The application does not have the rights to copy one of the specified objects.

</td>
</tr>
</table>

## -remarks

If the specified device supports copy operations to a functional storage, the <i>pszDestinationFolderObjectID</i> parameter may specify the identifier for a functional storage.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>