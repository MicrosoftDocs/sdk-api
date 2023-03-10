---
UID: NF:portabledeviceapi.IPortableDeviceContent2.UpdateObjectWithPropertiesAndData
title: IPortableDeviceContent2::UpdateObjectWithPropertiesAndData (portabledeviceapi.h)
description: Updates an object by using properties and data found on the device.
helpviewer_keywords: ["IPortableDeviceContent2 interface [Windows Portable Devices SDK]","UpdateObjectWithPropertiesAndData method","IPortableDeviceContent2.UpdateObjectWithPropertiesAndData","IPortableDeviceContent2::UpdateObjectWithPropertiesAndData","UpdateObjectWithPropertiesAndData","UpdateObjectWithPropertiesAndData method [Windows Portable Devices SDK]","UpdateObjectWithPropertiesAndData method [Windows Portable Devices SDK]","IPortableDeviceContent2 interface","portabledeviceapi/IPortableDeviceContent2::UpdateObjectWithPropertiesAndData","wpdsdk.iportabledevicecontent2_updateobjectwithpropertiesanddata"]
old-location: wpdsdk\iportabledevicecontent2_updateobjectwithpropertiesanddata.htm
tech.root: wpdsdk
ms.assetid: 43b8cf90-1c3f-43c2-a11f-cc4aef10bcf5
ms.date: 12/05/2018
ms.keywords: IPortableDeviceContent2 interface [Windows Portable Devices SDK],UpdateObjectWithPropertiesAndData method, IPortableDeviceContent2.UpdateObjectWithPropertiesAndData, IPortableDeviceContent2::UpdateObjectWithPropertiesAndData, UpdateObjectWithPropertiesAndData, UpdateObjectWithPropertiesAndData method [Windows Portable Devices SDK], UpdateObjectWithPropertiesAndData method [Windows Portable Devices SDK],IPortableDeviceContent2 interface, portabledeviceapi/IPortableDeviceContent2::UpdateObjectWithPropertiesAndData, wpdsdk.iportabledevicecontent2_updateobjectwithpropertiesanddata
req.header: portabledeviceapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: PortableDeviceAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPortableDeviceContent2::UpdateObjectWithPropertiesAndData
 - portabledeviceapi/IPortableDeviceContent2::UpdateObjectWithPropertiesAndData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceContent2.UpdateObjectWithPropertiesAndData
---

# IPortableDeviceContent2::UpdateObjectWithPropertiesAndData


## -description

The <b>UpdateObjectWithPropertiesAndData</b> method updates an object by using properties and data found on the device.

## -parameters

### -param pszObjectID [in]

The identifier of the object to update.

### -param pProperties [in]

The <a href="/windows/desktop/wpd_sdk/iportabledevicevalues">IPortableDeviceValues</a> interface that specifies the object properties to be updated.

### -param ppData [out]

The <b>IStream</b> interface through which the object data is sent to the device.

### -param pdwOptimalWriteBufferSize [in, out]

The optimal buffer size for writing the object data to <i>ppData</i>, or <b>NULL</b> if the buffer size is ignored.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed.

## -remarks

Device formats and object formats can derive some of their object properties from the data itself. Or, they can  have property values  that depend on the data. For example, a music track has a duration property that is specified when an application calls the <a href="/windows/desktop/api/portabledeviceapi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata">IPortableDeviceContent::CreateObjectWithPropertiesAndData</a> method. If this track is stored as a default resource (<a href="/windows/desktop/wpd_sdk/wpd-resource-default">WPD_RESOURCE_DEFAULT</a>), the application might update it. The application additionally mighthave to update the duration property. This method lets the application perform both updates at the same time.

An update is incomplete until the <b>IStream::Commit</b> method is called on the object referenced by the <i>ppData</i> parameter.

To abandon a data transfer in progress, an application should call the <b>IStream::Revert</b> method on the object referenced by the <i>ppData</i> parameter.

The <b>IStream</b> interface object referenced by the <i>ppData</i> parameter must be released after the update operation is complete, or, is canceled.