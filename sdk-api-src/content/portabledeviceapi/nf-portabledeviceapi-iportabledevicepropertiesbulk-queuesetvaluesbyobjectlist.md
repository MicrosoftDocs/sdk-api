---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulk.QueueSetValuesByObjectList
title: IPortableDevicePropertiesBulk::QueueSetValuesByObjectList
author: windows-sdk-content
description: The QueueSetValuesByObjectList method queues a request to set one or more specified values on one or more specified objects on the device.
old-location: wpdsdk\iportabledevicepropertiesbulk_queuesetvaluesbyobjectlist.htm
tech.root: wpd_sdk
ms.assetid: cfb03354-e395-4fb7-aa76-a1f786ccd71c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],QueueSetValuesByObjectList method, IPortableDevicePropertiesBulk.QueueSetValuesByObjectList, IPortableDevicePropertiesBulk::QueueSetValuesByObjectList, IPortableDevicePropertiesBulkQueueSetValuesByObjectList, QueueSetValuesByObjectList, QueueSetValuesByObjectList method [Windows Portable Devices SDK], QueueSetValuesByObjectList method [Windows Portable Devices SDK],IPortableDevicePropertiesBulk interface, portabledeviceapi/IPortableDevicePropertiesBulk::QueueSetValuesByObjectList, wpdsdk.iportabledevicepropertiesbulk_queuesetvaluesbyobjectlist
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IPortableDevicePropertiesBulk.QueueSetValuesByObjectList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDevicePropertiesBulk::QueueSetValuesByObjectList


## -description



The <b>QueueSetValuesByObjectList</b> method queues a request to set one or more specified values on one or more specified objects on the device.




## -parameters




### -param pObjectValues [in]

Pointer to an <a href="https://msdn.microsoft.com/8bce9d27-f240-41ec-acf4-fefccdd95e9f">IPortableDeviceValuesCollection</a> interface that contains the properties and values to set on specified objects. This interface holds one or more <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interfaces, each representing a single object. Each <b>IPortableDeviceValues</b> interface holds a collection of key/value pairs, where the key is the <b>PROPERTYKEY</b> identifying the property, and the value is a data type that varies by property. Each <b>IPortableDeviceValues</b> interface also holds one WPD_OBJECT_ID property that identifies the object to which this interface refers.


### -param pCallback [in]

Pointer to an application-implemented <a href="https://msdn.microsoft.com/0a066e30-f584-4a8f-be08-c542060a335b">IPortableDevicePropertiesBulkCallback</a> interface that will receive the information as it is retrieved.


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



The queued request is not started until the application calls <a href="https://msdn.microsoft.com/a69afdc9-622d-45fc-b71e-6058d9d528b0">Start</a>. For more information on how to use this method, see <a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk Interface</a>.




## -see-also




<a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk Interface</a>



<a href="https://msdn.microsoft.com/0c29777c-4125-46a1-94b2-8d70374e566a">IPortableDevicePropertiesBulk::QueueGetValuesByObjectList</a>
 

 

