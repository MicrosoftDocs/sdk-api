---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IPortableDeviceServiceCapabilities::GetSupportedFormatProperties


## -description


The <b>GetSupportedFormatProperties</b> method retrieves the properties supported by the service for the specified format.


## -parameters




### -param Format [in]

The format whose properties are retrieved.


### -param ppKeys [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597583">IPortableDeviceKeyCollection</a> interface that receives the list of properties.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



The retrieved property collection is a superset of all properties supported by an object of the specified format.

An application can also retrieve the properties for an object by calling the <a href="https://msdn.microsoft.com/c6c42347-145c-4be7-bea6-34b13c211cb1">IPortableDeviceService::SendCommand</a> method with the <a href="https://msdn.microsoft.com/library/windows/hardware/ff597796">WPD_COMMAND_OBJECT_PROPERTIES_GET_SUPPORTED</a> property passed as the command identifier. However, the <b>GetSupportedFormatProperties</b> method is typically faster than the <b>IPortableDeviceService::SendCommand</b> method.




## -see-also




<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>
 

 

