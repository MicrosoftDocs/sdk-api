---
UID: NF:portabledeviceapi.IPortableDeviceContent.Delete
title: IPortableDeviceContent::Delete (portabledeviceapi.h)
description: The Delete method deletes one or more objects from the device.
helpviewer_keywords: ["Delete","Delete method [Windows Portable Devices SDK]","Delete method [Windows Portable Devices SDK]","IPortableDeviceContent interface","IPortableDeviceContent interface [Windows Portable Devices SDK]","Delete method","IPortableDeviceContent.Delete","IPortableDeviceContent::Delete","IPortableDeviceContentDelete","portabledeviceapi/IPortableDeviceContent::Delete","wpdsdk.iportabledevicecontent_delete"]
old-location: wpdsdk\iportabledevicecontent_delete.htm
tech.root: wpdsdk
ms.assetid: 7315c869-d2b6-4ccf-9315-ec1fc1d827ac
ms.date: 12/05/2018
ms.keywords: Delete, Delete method [Windows Portable Devices SDK], Delete method [Windows Portable Devices SDK],IPortableDeviceContent interface, IPortableDeviceContent interface [Windows Portable Devices SDK],Delete method, IPortableDeviceContent.Delete, IPortableDeviceContent::Delete, IPortableDeviceContentDelete, portabledeviceapi/IPortableDeviceContent::Delete, wpdsdk.iportabledevicecontent_delete
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
 - IPortableDeviceContent::Delete
 - portabledeviceapi/IPortableDeviceContent::Delete
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
 - IPortableDeviceContent.Delete
---

# IPortableDeviceContent::Delete


## -description

The <b>Delete</b> method deletes one or more objects from the device.

## -parameters

### -param dwOptions [in]

One of the <a href="/windows/desktop/wpd_sdk/delete-object-options">DELETE_OBJECT_OPTIONS</a> enumerators.

### -param pObjectIDs [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that holds one or more null-terminated strings (type VT_LPWSTR) specifying the object IDs of the objects to delete.

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
At least one object could not be deleted. The <i>ppResults</i> parameter, if specified, contains the per-object error code.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_XXXXXXXX</b></dt>
</dl>
</td>
<td width="60%">
The driver did not delete any objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid value was specified for <i>dwOptions</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The application does not have permission to delete the object.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_DIR_NOT_EMPTY)</b></dt>
</dl>
</td>
<td width="60%">
The specified folder or directory could not be deleted because it was not empty.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_INVALID_OPERATION)</b></dt>
</dl>
</td>
<td width="60%">
The application specified PORTABLE_DEVICE_DELETE_NO_RECURSION, and the object has children.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(ERROR_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
The object could not be deleted because it does not exist on the device.

</td>
</tr>
</table>

## -remarks

To see if recursive deletion is supported, call <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions">IPortableDeviceCapabilities::GetCommandOptions</a>. If the retrieved <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface contains a property value called WPD_OPTION_OBJECT_MANAGEMENT_RECURSIVE_DELETE_SUPPORTED with a <i>boolVal</i> value of True, the device supports recursive deletion.
      

The following table lists the possible return codes that may appear in the collection at which <i>ppResults</i> points.
      


#### Examples

For an example of how to use this method, see <a href="/windows/desktop/wpd_sdk/deleting-content-from-the-device">Deleting Content from the Device</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/wpd_sdk/deleting-content-from-the-device">Deleting Content from the Device</a>



<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent">IPortableDeviceContent Interface</a>