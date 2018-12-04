---
UID: NF:portabledeviceapi.IPortableDeviceContent2.UpdateObjectWithPropertiesAndData
title: IPortableDeviceContent2::UpdateObjectWithPropertiesAndData
author: windows-sdk-content
description: Updates an object by using properties and data found on the device.
old-location: wpdsdk\iportabledevicecontent2_updateobjectwithpropertiesanddata.htm
tech.root: wpd_sdk
ms.assetid: 43b8cf90-1c3f-43c2-a11f-cc4aef10bcf5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPortableDeviceContent2 interface [Windows Portable Devices SDK],UpdateObjectWithPropertiesAndData method, IPortableDeviceContent2.UpdateObjectWithPropertiesAndData, IPortableDeviceContent2::UpdateObjectWithPropertiesAndData, UpdateObjectWithPropertiesAndData, UpdateObjectWithPropertiesAndData method [Windows Portable Devices SDK], UpdateObjectWithPropertiesAndData method [Windows Portable Devices SDK],IPortableDeviceContent2 interface, portabledeviceapi/IPortableDeviceContent2::UpdateObjectWithPropertiesAndData, wpdsdk.iportabledevicecontent2_updateobjectwithpropertiesanddata
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - PortableDeviceAPI.h
api_name:
 - IPortableDeviceContent2.UpdateObjectWithPropertiesAndData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPortableDeviceContent2::UpdateObjectWithPropertiesAndData


## -description


The <b>UpdateObjectWithPropertiesAndData</b> method updates an object by using properties and data found on the device. 


## -parameters




### -param pszObjectID [in]

The identifier of the object to update.


### -param pProperties [in]

The <a href="https://msdn.microsoft.com/a73cbb4e-15d2-4c8d-9267-aaec9a0fd09f">IPortableDeviceValues</a> interface that specifies the object properties to be updated.


### -param ppData [out]

The <b>IStream</b> interface through which the object data is sent to the device.


### -param pdwOptimalWriteBufferSize [in, out]

The optimal buffer size for writing the object data to <i>ppData</i>, or <b>NULL</b> if the buffer size is ignored.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Device formats and object formats can derive some of their object properties from the data itself. Or, they can  have property values  that depend on the data. For example, a music track has a duration property that is specified when an application calls the <a href="https://msdn.microsoft.com/ea3445cc-69af-40a6-a5a4-695e0f2e1fb6">IPortableDeviceContent::CreateObjectWithPropertiesAndData</a> method. If this track is stored as a default resource (<a href="https://msdn.microsoft.com/e534ea86-4932-45c7-87e7-03926202fa7e">WPD_RESOURCE_DEFAULT</a>), the application might update it. The application additionally mighthave to update the duration property. This method lets the application perform both updates at the same time.

An update is incomplete until the <b>IStream::Commit</b> method is called on the object referenced by the <i>ppData</i> parameter.

To abandon a data transfer in progress, an application should call the <b>IStream::Revert</b> method on the object referenced by the <i>ppData</i> parameter.

The <b>IStream</b> interface object referenced by the <i>ppData</i> parameter must be released after the update operation is complete, or, is canceled. 



