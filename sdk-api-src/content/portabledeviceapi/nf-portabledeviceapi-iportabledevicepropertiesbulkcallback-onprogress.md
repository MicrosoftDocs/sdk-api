---
UID: NF:portabledeviceapi.IPortableDevicePropertiesBulkCallback.OnProgress
title: IPortableDevicePropertiesBulkCallback::OnProgress (portabledeviceapi.h)
description: The OnProgress method is called by the SDK when a bulk operation started by IPortableDevicePropertiesBulk::Start has sent data to the device and received some information back.
helpviewer_keywords: ["IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK]","OnProgress method","IPortableDevicePropertiesBulkCallback.OnProgress","IPortableDevicePropertiesBulkCallback::OnProgress","IPortableDevicePropertiesBulkCallbackOnProgress","OnProgress","OnProgress method [Windows Portable Devices SDK]","OnProgress method [Windows Portable Devices SDK]","IPortableDevicePropertiesBulkCallback interface","portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnProgress","wpdsdk.iportabledevicepropertiesbulkcallback_onprogress"]
old-location: wpdsdk\iportabledevicepropertiesbulkcallback_onprogress.htm
tech.root: wpdsdk
ms.assetid: f357d7da-00cd-4439-af6d-5d3716a8443b
ms.date: 12/05/2018
ms.keywords: IPortableDevicePropertiesBulkCallback interface [Windows Portable Devices SDK],OnProgress method, IPortableDevicePropertiesBulkCallback.OnProgress, IPortableDevicePropertiesBulkCallback::OnProgress, IPortableDevicePropertiesBulkCallbackOnProgress, OnProgress, OnProgress method [Windows Portable Devices SDK], OnProgress method [Windows Portable Devices SDK],IPortableDevicePropertiesBulkCallback interface, portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnProgress, wpdsdk.iportabledevicepropertiesbulkcallback_onprogress
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
 - IPortableDevicePropertiesBulkCallback::OnProgress
 - portabledeviceapi/IPortableDevicePropertiesBulkCallback::OnProgress
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
 - IPortableDevicePropertiesBulkCallback.OnProgress
---

# IPortableDevicePropertiesBulkCallback::OnProgress


## -description

The <b>OnProgress</b> method is called by the SDK when a bulk operation started by <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-start">IPortableDevicePropertiesBulk::Start</a> has sent data to the device and received some information back.

## -parameters

### -param pContext [in]

Pointer to a GUID that identifies which operation is in progress. This value is produced by a <b>Queue</b>... method of the <a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulk">IPortableDevicePropertiesBulk</a> interface.

### -param pResults [in]

Pointer to an <a href="/windows/desktop/wpd_sdk/iportabledevicevaluescollection">IPortableDeviceValuesCollection</a> interface that contains the results retrieved from the device. This interface will hold one or more <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interfaces. Each of these interfaces will hold one <a href="/windows/desktop/wpd_sdk/object-properties">WPD_OBJECT_ID</a> property with a string value (VT_LPSTR) specifying the object ID of the object that these values pertain to. The rest of the values in each <b>IPortableDeviceValues</b> interface vary, depending on the bulk operation being reported. For the <b>QueueGetValuesByObjectFormat</b> and <b>QueueGetValuesByObjectList</b> methods, they will be retrieved values of varying types. For <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicepropertiesbulk-queuesetvaluesbyobjectlist">QueueSetValuesByObjectList</a>, they will be <b>VT_ERROR</b><b>HRESULT</b> values for any errors encountered when setting values.

## -returns

The application should return either S_OK, or an error code to abandon the operation. All error codes are handled the same way.

## -remarks

This method can be called once or multiple times, depending on how large the operation is.

This method does not necessarily retrieve all properties at once, nor does it return the properties in a particular order.

If this method is called multiple times, it may return properties for the same object identifier each time.

## -see-also

<a href="/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback">IPortableDevicePropertiesBulkCallback Interface</a>