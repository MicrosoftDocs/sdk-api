---
UID: NF:portabledeviceapi.IPortableDeviceContent.Move
title: IPortableDeviceContent::Move (portabledeviceapi.h)
description: The Move method moves one or more objects from one location on the device to another.
helpviewer_keywords: ["IPortableDeviceContent interface [Windows Portable Devices SDK]","Move method","IPortableDeviceContent.Move","IPortableDeviceContent::Move","IPortableDeviceContentMove","Move","Move method [Windows Portable Devices SDK]","Move method [Windows Portable Devices SDK]","IPortableDeviceContent interface","portabledeviceapi/IPortableDeviceContent::Move","wpdsdk.iportabledevicecontent_move"]
old-location: wpdsdk\iportabledevicecontent_move.htm
tech.root: wpdsdk
ms.assetid: 938a6a06-31c5-44d1-b87b-a108995ae9a1
ms.date: 12/05/2018
ms.keywords: IPortableDeviceContent interface [Windows Portable Devices SDK],Move method, IPortableDeviceContent.Move, IPortableDeviceContent::Move, IPortableDeviceContentMove, Move, Move method [Windows Portable Devices SDK], Move method [Windows Portable Devices SDK],IPortableDeviceContent interface, portabledeviceapi/IPortableDeviceContent::Move, wpdsdk.iportabledevicecontent_move
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
 - IPortableDeviceContent::Move
 - portabledeviceapi/IPortableDeviceContent::Move
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
 - IPortableDeviceContent.Move
---

# IPortableDeviceContent::Move


## -description

The <b>Move</b> method moves one or more objects from one location on the device to another.

## -parameters

### -param pObjectIDs [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that holds one or more null-terminated strings (type VT_LPWSTR) specifying the object IDs of the objects to be moved.

### -param pszDestinationFolderObjectID [in]

Pointer to a null-terminated string that specifies the ID of the destination.

### -param ppResults [in, out]

Optional. On return, this parameter contains a collection of VT_ERROR values indicating the success or failure of the operation. The first element returned in <i>ppResults</i> corresponds to the first object in the <i>pObjectIDs</i> collection, the second element returned in <i>ppResults</i> corresponds to the second object in the <i>pObjectIDs</i> collection, and so on. This parameter can be <b>NULL</b> if the application is not concerned with the results.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table. If any error value is returned, no objects were deleted on the device.
          

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
One or more objects were deleted, but at least one object could not be deleted. See <i>ppFailedObjectIDs</i> to learn which objects were not be deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The application does not have the rights to move the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
At least one of the required arguments was a <b>NULL</b> pointer.

</td>
</tr>
</table>

## -remarks

If the specified device supports move operations on a functional storage, the <i>pszDestinationFolderObjectID</i> parameter may specify the identifier for a functional storage.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/moving-content-on-the-device">Moving Content on the Device</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>



<a href="/windows/desktop/wpd_sdk/moving-content-on-the-device">Moving Content on the Device</a>