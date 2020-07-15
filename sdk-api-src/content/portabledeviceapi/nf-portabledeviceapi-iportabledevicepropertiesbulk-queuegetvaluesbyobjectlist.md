---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulk.QueueGetValuesByObjectList
title: IPortableDevicePropertiesBulk::QueueGetValuesByObjectList (portabledeviceapi.h)
description: The QueueGetValuesByObjectList method queues a request for one or more specified properties from one or more specified objects on the device.
helpviewer_keywords: ["IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK]","QueueGetValuesByObjectList method","IPortableDevicePropertiesBulk.QueueGetValuesByObjectList","IPortableDevicePropertiesBulk::QueueGetValuesByObjectList","IPortableDevicePropertiesBulkQueueGetValuesByObjectList","QueueGetValuesByObjectList","QueueGetValuesByObjectList method [Windows Portable Devices SDK]","QueueGetValuesByObjectList method [Windows Portable Devices SDK]","IPortableDevicePropertiesBulk interface","portabledeviceapi/IPortableDevicePropertiesBulk::QueueGetValuesByObjectList","wpdsdk.iportabledevicepropertiesbulk_queuegetvaluesbyobjectlist"]
old-location: wpdsdk\iportabledevicepropertiesbulk_queuegetvaluesbyobjectlist.htm
tech.root: wpd_sdk
ms.assetid: 0c29777c-4125-46a1-94b2-8d70374e566a
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],QueueGetValuesByObjectList method, IPortableDevicePropertiesBulk.QueueGetValuesByObjectList, IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, IPortableDevicePropertiesBulkQueueGetValuesByObjectList, QueueGetValuesByObjectList, QueueGetValuesByObjectList method [Windows Portable Devices SDK], QueueGetValuesByObjectList method [Windows Portable Devices SDK],IPortableDevicePropertiesBulk interface, portabledeviceapi/IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, wpdsdk.iportabledevicepropertiesbulk_queuegetvaluesbyobjectlist
f1_keywords:
- portabledeviceapi/IPortableDevicePropertiesBulk.QueueGetValuesByObjectList
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
- IPortableDevicePropertiesBulk.QueueGetValuesByObjectList
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPortableDevicePropertiesBulk::QueueGetValuesByObjectList


## -description



The <b>QueueGetValuesByObjectList</b> method queues a request for one or more specified properties from one or more specified objects on the device.




## -parameters




### -param pObjectIDs [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicepropvariantcollection">IPortableDevicePropVariantCollection</a> interface that lists the object IDs of all the objects to query. These will be of type VT_LPWSTR.


### -param pKeys [in]

Pointer to an <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/iportabledevicekeycollection">IPortableDeviceKeyCollection</a> interface that specifies the properties to request. For a list of properties defined by Windows Portable Devices, see <a href="https://docs.microsoft.com/windows/desktop/wpd_sdk/properties-and-attributes">Properties and Attributes</a>. Specify <b>NULL</b> to indicate all properties from the specified objects.


### -param pCallback [in]

Pointer to an application-implemented <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback">IPortableDevicePropertiesBulkCallback</a> interface that will receive the information as it is retrieved.


### -param pContext [out]

Pointer to a GUID that is used to start, cancel, or identify the request <b>IPortableDevicePropertiesBulkCallback</b> callbacks, if implemented.


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



The queued request is not started until the application calls <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start">Start</a>. For more information on how to use this method, see <a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk Interface</a>.

Due to performance issues, some devices may not return a comprehensive list of properties when the <i>pKeys</i> parameter is <b>NULL</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist">IPortableDevicePropertiesBulk::QueueSetValuesByObjectList</a>
 

 

