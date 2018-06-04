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

# INSSBuffer4::GetPropertyByIndex


## -description



The <b>GetPropertyByIndex</b> method retrieves a buffer property, also called a data unit extension, that was set using <a href="https://msdn.microsoft.com/5aede025-65ae-4615-9511-af22b8c0dc00">INSSBuffer3::SetProperty</a>. This method differs from <a href="https://msdn.microsoft.com/b7733df5-f764-4996-b324-fa050b1db0af">INSSBuffer3::GetProperty</a> in that, instead of accessing the property by name, it uses an index ranging from zero to one less than the total number of properties associated with the sample.




## -parameters




### -param dwBufferPropertyIndex [in]

<b>DWORD</b> containing the buffer property index. This value will be between zero and one less than the total number of properties associated with the sample. You can retrieve the total number of properties by calling <a href="https://msdn.microsoft.com/b47f26b3-e816-498d-adc3-c6d3357971e6">INSSBuffer4::GetPropertyCount</a>.


### -param pguidBufferProperty [out]

Pointer to a GUID specifying the type of buffer property.


### -param pvBufferProperty [out]

Void pointer containing the value of the buffer property.


### -param pdwBufferPropertySize [in, out]

Pointer to a <b>DWORD</b> containing the size of the value pointed to by <i>pvBufferProperty</i>. If you set <i>pvBufferProperty</i> to <b>NULL</b>, this value will be set to the required size in bytes of the buffer needed to store the property value.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/d6531e52-b58b-46ed-a47b-444cd98e1ec5">INSSBuffer4 Interface</a>
 

 

