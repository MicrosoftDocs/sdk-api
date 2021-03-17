---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulk.QueueSetValuesByObjectList
title: IPortableDevicePropertiesBulk::QueueSetValuesByObjectList (portabledeviceapi.h)
description: The QueueSetValuesByObjectList method queues a request to set one or more specified values on one or more specified objects on the device.
helpviewer_keywords: ["IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK]","QueueSetValuesByObjectList method","IPortableDevicePropertiesBulk.QueueSetValuesByObjectList","IPortableDevicePropertiesBulk::QueueSetValuesByObjectList","IPortableDevicePropertiesBulkQueueSetValuesByObjectList","QueueSetValuesByObjectList","QueueSetValuesByObjectList method [Windows Portable Devices SDK]","QueueSetValuesByObjectList method [Windows Portable Devices SDK]","IPortableDevicePropertiesBulk interface","portabledeviceapi/IPortableDevicePropertiesBulk::QueueSetValuesByObjectList","wpdsdk.iportabledevicepropertiesbulk_queuesetvaluesbyobjectlist"]
old-location: wpdsdk\iportabledevicepropertiesbulk_queuesetvaluesbyobjectlist.htm
tech.root: wpdsdk
ms.assetid: cfb03354-e395-4fb7-aa76-a1f786ccd71c
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],QueueSetValuesByObjectList method, IPortableDevicePropertiesBulk.QueueSetValuesByObjectList, IPortableDevicePropertiesBulk::QueueSetValuesByObjectList, IPortableDevicePropertiesBulkQueueSetValuesByObjectList, QueueSetValuesByObjectList, QueueSetValuesByObjectList method [Windows Portable Devices SDK], QueueSetValuesByObjectList method [Windows Portable Devices SDK],IPortableDevicePropertiesBulk interface, portabledeviceapi/IPortableDevicePropertiesBulk::QueueSetValuesByObjectList, wpdsdk.iportabledevicepropertiesbulk_queuesetvaluesbyobjectlist
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
 - IPortableDevicePropertiesBulk::QueueSetValuesByObjectList
 - portabledeviceapi/IPortableDevicePropertiesBulk::QueueSetValuesByObjectList
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
 - IPortableDevicePropertiesBulk.QueueSetValuesByObjectList
---

# IPortableDevicePropertiesBulk::QueueSetValuesByObjectList


## -description

The <b>QueueSetValuesByObjectList</b> method queues a request to set one or more specified values on one or more specified objects on the device.

## -parameters

### -param pObjectValues [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevaluescollection">IPortableDeviceValuesCollection</a> interface that contains the properties and values to set on specified objects. This interface holds one or more <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interfaces, each representing a single object. Each <b>IPortableDeviceValues</b> interface holds a collection of key/value pairs, where the key is the <b>PROPERTYKEY</b> identifying the property, and the value is a data type that varies by property. Each <b>IPortableDeviceValues</b> interface also holds one WPD_OBJECT_ID property that identifies the object to which this interface refers.

### -param pCallback [in]

Pointer to an application-implemented <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback">IPortableDevicePropertiesBulkCallback</a> interface that will receive the information as it is retrieved.

### -param pContext [out]

Pointer to a GUID that is used to start, cancel, or identify the request to any client-implemented <b>IPortableDevicePropertiesBulkCallback</b> callbacks.

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

The queued request is not started until the application calls <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start">Start</a>. For more information on how to use this method, see <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk Interface</a>.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk Interface</a>



<a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuegetvaluesbyobjectlist">IPortableDevicePropertiesBulk::QueueGetValuesByObjectList</a>