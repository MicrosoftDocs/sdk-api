---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulkCallback.OnProgress
title: IPortableDevicePropertiesBulkCallback::OnProgress
author: windows-sdk-content
description: The OnProgress method is called by the SDK when a bulk operation started by IPortableDevicePropertiesBulk::Start has sent data to the device and received some information back.
old-location: wpdsdk\iportabledevicepropertiesbulkcallback_onprogress.htm
tech.root: wpd_sdk
ms.assetid: f357d7da-00cd-4439-af6d-5d3716a8443b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK],OnProgress method, IPortableDevicePropertiesBulkCallback.OnProgress, IPortableDevicePropertiesBulkCallback::OnProgress, IPortableDevicePropertiesBulkCallbackOnProgress, OnProgress, OnProgress method [Windows Portable Devices SDK], OnProgress method [Windows Portable Devices SDK],IPortableDevicePropertiesBulkCallback interface, portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnProgress, wpdsdk.iportabledevicepropertiesbulkcallback_onprogress
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
 - IPortableDevicePropertiesBulkCallback.OnProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDevicePropertiesBulkCallback::OnProgress


## -description



The <b>OnProgress</b> method is called by the SDK when a bulk operation started by <a href="https://msdn.microsoft.com/a69afdc9-622d-45fc-b71e-6058d9d528b0">IPortableDevicePropertiesBulk::Start</a> has sent data to the device and received some information back.




## -parameters




### -param pContext [in]

Pointer to a GUID that identifies which operation is in progress. This value is produced by a <b>Queue</b>... method of the <a href="https://msdn.microsoft.com/57cda40a-8573-4b6c-981e-770f35186038">IPortableDevicePropertiesBulk</a> interface.


### -param pResults [in]

Pointer to an <a href="https://msdn.microsoft.com/8bce9d27-f240-41ec-acf4-fefccdd95e9f">IPortableDeviceValuesCollection</a> interface that contains the results retrieved from the device. This interface will hold one or more <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interfaces. Each of these interfaces will hold one <a href="https://msdn.microsoft.com/en-us/library/Dd375704(v=VS.85).aspx">WPD_OBJECT_ID</a> property with a string value (VT_LPSTR) specifying the object ID of the object that these values pertain to. The rest of the values in each <b>IPortableDeviceValues</b> interface vary, depending on the bulk operation being reported. For the <b>QueueGetValuesByObjectFormat</b> and <b>QueueGetValuesByObjectList</b> methods, they will be retrieved values of varying types. For <a href="https://msdn.microsoft.com/cfb03354-e395-4fb7-aa76-a1f786ccd71c">QueueSetValuesByObjectList</a>, they will be <b>VT_ERROR</b><b>HRESULT</b> values for any errors encountered when setting values.


## -returns



The application should return either S_OK, or an error code to abandon the operation. All error codes are handled the same way.




## -remarks



This method can be called once or multiple times, depending on how large the operation is.

This method does not necessarily retrieve all properties at once, nor does it return the properties in a particular order.

If this method is called multiple times, it may return properties for the same object identifier each time.




## -see-also




<a href="https://msdn.microsoft.com/0a066e30-f584-4a8f-be08-c542060a335b">IPortableDevicePropertiesBulkCallback Interface</a>
 

 

