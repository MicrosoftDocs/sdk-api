---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulk.QueueGetValuesByObjectList
title: IPortableDevicePropertiesBulk::QueueGetValuesByObjectList
author: windows-sdk-content
description: The QueueGetValuesByObjectList method queues a request for one or more specified properties from one or more specified objects on the device.
old-location: wpdsdk\iportabledevicepropertiesbulk_queuegetvaluesbyobjectlist.htm
old-project: wpd_sdk
ms.assetid: 0c29777c-4125-46a1-94b2-8d70374e566a
ms.author: windowssdkdev
ms.date: 04/11/2018
ms.keywords: IPortableDevicePropertiesBulk interface [Windows Portable Devices SDK],QueueGetValuesByObjectList method, IPortableDevicePropertiesBulk.QueueGetValuesByObjectList, IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, IPortableDevicePropertiesBulkQueueGetValuesByObjectList, QueueGetValuesByObjectList, QueueGetValuesByObjectList method [Windows Portable Devices SDK], QueueGetValuesByObjectList method [Windows Portable Devices SDK],IPortableDevicePropertiesBulk interface, portabledeviceapi/IPortableDevicePropertiesBulk::QueueGetValuesByObjectList, wpdsdk.iportabledevicepropertiesbulk_queuegetvaluesbyobjectlist
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PNRPINFO_V2, *PPNRPINFO_V2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	PortableDeviceGUIDs.lib
-	PortableDeviceGUIDs.dll
api_name:
-	IPortableDevicePropertiesBulk.QueueGetValuesByObjectList
product: Windows
targetos: Windows
req.lib: PortableDeviceGUIDs.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IPortableDevicePropertiesBulk::QueueGetValuesByObjectList


## -description



The <b>QueueGetValuesByObjectList</b> method queues a request for one or more specified properties from one or more specified objects on the device.




## -parameters




### -param pObjectIDs [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597589">IPortableDevicePropVariantCollection</a> interface that lists the object IDs of all the objects to query. These will be of type VT_LPWSTR.


### -param pKeys [in]

Pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff597583">IPortableDeviceKeyCollection</a> interface that specifies the properties to request. For a list of properties defined by Windows Portable Devices, see <a href="https://msdn.microsoft.com/3bfbe8d0-6ad5-42de-afdd-d83328aaaa62">Properties and Attributes</a>. Specify <b>NULL</b> to indicate all properties from the specified objects.


### -param pCallback [in]

Pointer to an application-implemented <a href="https://msdn.microsoft.com/0a066e30-f584-4a8f-be08-c542060a335b">IPortableDevicePropertiesBulkCallback</a> interface that will receive the information as it is retrieved.


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



The queued request is not started until the application calls <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>. For more information on how to use this method, see <a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk Interface</a>.

Due to performance issues, some devices may not return a comprehensive list of properties when the <i>pKeys</i> parameter is <b>NULL</b>.




## -see-also




<a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk Interface</a>



<a href="https://msdn.microsoft.com/cfb03354-e395-4fb7-aa76-a1f786ccd71c">IPortableDevicePropertiesBulk::QueueSetValuesByObjectList</a>
 

 

