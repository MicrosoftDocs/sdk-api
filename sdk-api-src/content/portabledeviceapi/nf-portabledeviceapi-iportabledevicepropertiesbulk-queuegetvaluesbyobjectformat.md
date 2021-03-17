---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulk.QueueGetValuesByObjectFormat
title: IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat (portabledeviceapi.h)
description: The QueueGetValuesByObjectFormat interface queues a request for properties of objects of a specific format on a device.
helpviewer_keywords: ["IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK]","QueueGetValuesByObjectFormat method","IPortableDevicePropertiesBulk.QueueGetValuesByObjectFormat","IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat","IPortableDevicePropertiesBulkQueueGetValuesByObjectFormat","QueueGetValuesByObjectFormat","QueueGetValuesByObjectFormat method [Windows Portable Devices SDK]","QueueGetValuesByObjectFormat method [Windows Portable Devices SDK]","IPortableDevicePropertiesBulk interface","portabledeviceapi/IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat","wpdsdk.iportabledevicepropertiesbulk_queuegetvaluesbyobjectformat"]
old-location: wpdsdk\iportabledevicepropertiesbulk_queuegetvaluesbyobjectformat.htm
tech.root: wpdsdk
ms.assetid: a52b45b5-fd9b-4af5-bb82-293816190e38
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],QueueGetValuesByObjectFormat method, IPortableDevicePropertiesBulk.QueueGetValuesByObjectFormat, IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat, IPortableDevicePropertiesBulkQueueGetValuesByObjectFormat, QueueGetValuesByObjectFormat, QueueGetValuesByObjectFormat method [Windows Portable Devices SDK], QueueGetValuesByObjectFormat method [Windows Portable Devices SDK],IPortableDevicePropertiesBulk interface, portabledeviceapi/IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat, wpdsdk.iportabledevicepropertiesbulk_queuegetvaluesbyobjectformat
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
 - IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat
 - portabledeviceapi/IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat
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
 - IPortableDevicePropertiesBulk.QueueGetValuesByObjectFormat
---

# IPortableDevicePropertiesBulk::QueueGetValuesByObjectFormat


## -description

The <b>QueueGetValuesByObjectFormat</b> interface queues a request for properties of objects of a specific format on a device.

## -parameters

### -param pguidObjectFormat [in]

Pointer to a <b>GUID</b> that specifies the object format. Only objects of this type are queried.

### -param pszParentObjectID [in]

Pointer to a null-terminated string that contains the object ID of the parent object where the search should begin. To search all the objects on a device, specify <b>WPD_DEVICE_OBJECT_ID</b>.

### -param dwDepth [in]

The maximum depth to search below the parent, where 1 means immediate children only. It is acceptable for this number to be greater than the actual number of levels. To search to any depth, specify 0xFFFFFFFF

### -param pKeys [in]

Pointer to an <b>IPortableDeviceKeyCollection</b> interface that contains the properties to retrieve. For a list of properties that are defined by Windows Portable Devices, see <a href="/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a>. Specify <b>NULL</b> to indicate all properties from the specified format.

### -param pCallback [in]

Pointer to an application-implemented <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback">IPortableDevicePropertiesBulkCallback</a> interface that will receive the information as it is retrieved.

### -param pContext [out]

Pointer to a GUID that will be used to start, cancel, or identify the request in <b>IPortableDevicePropertiesBulkCallback</b> callbacks, if implemented.

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
The operation was queued successfully.

</td>
</tr>
</table>

## -remarks

If you specify WPD_OBJECT_FORMAT_ALL for the <i>pguidObjectFormat</i> parameter, this method will return properties for all objects on the device.

If the <i>pszParentObjectID</i> parameter is set to an empty string (""), the method will perform a search that is dependent on the <i>dwDepth</i> parameter as described in the following table.

<table>
<tr>
<td><b>dwDepth</b></td>
<td><b>Method returns</b></td>
</tr>
<tr>
<td>0</td>
<td>No results</td>
</tr>
<tr>
<td>1</td>
<td>Values for the specified device only.</td>
</tr>
<tr>
<td>2</td>
<td>Values for the specified device and all functional objects found on that device.</td>
</tr>
</table>
 

If the <i>pszParentObjectID</i> parameter is set to WPD_DEVICE_OBJECT_ID, the method will perform a search that is dependent on the <i>dwDepth</i> parameter as described in the following table.

<table>
<tr>
<td><b>dwDepth</b></td>
<td><b>Method returns</b></td>
</tr>
<tr>
<td>0</td>
<td>Values for the specified device only.</td>
</tr>
<tr>
<td>1</td>
<td>Values for the specified device and all functional objects found on that device.</td>
</tr>
</table>
 

The queued request is not started until the application calls <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start">Start</a>. For more information on how to use this method, see <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk Interface</a>.

Due to performance issues, some devices may not return a comprehensive list of properties when the <i>pKeys</i> parameter is <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk Interface</a>