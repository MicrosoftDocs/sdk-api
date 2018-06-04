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

# IPortableDeviceServiceCapabilities::GetMethodAttributes


## -description


The <b>GetMethodAttributes</b> method retrieves the attributes used to describe a given method.


## -parameters




### -param Method [in]

The method whose attributes are retrieved.


### -param ppAttributes [out]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface that receives the list of attributes.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Any other <b>HRESULT</b> value indicates that the call failed. 
          




## -remarks



Possible attributes include the <a href="wpd_attributes.htm">WPD_METHOD_ATTRIBUTE_NAME</a>, <b>WPD_METHOD_ATTRIBUTE_ASSOCIATED_FORMAT</b>, <b>WPD_METHOD_ATTRIBUTE_ACCESS</b>, and <a href="wpd_method_attributes.htm">WPD_METHOD_ATTRIBUTE_PARAMETERS</a> properties.
      


#### Examples

For an example of how to use this method, see <a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff597562">Device Interface GUIDs</a>



<a href="https://msdn.microsoft.com/d472d31c-90da-4ecc-9cf7-4474457a244f">IPortableDeviceServiceCapabilities Interface</a>



<a href="https://msdn.microsoft.com/a7708c60-758a-4fb6-8ef9-074ecdc9cf60">Method, Format, and Parameter Attributes</a>



<a href="https://msdn.microsoft.com/783a6552-9b22-4af4-9252-b443e2624687">Retrieving Supported Service Methods</a>
 

 

