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

# IWMStreamConfig2::AddDataUnitExtension


## -description



The <b>AddDataUnitExtension</b> method adds a data unit extension system to the stream. You can use data unit extension systems to attach custom data to samples in an output file.




## -parameters




### -param guidExtensionSystemID [in]

A GUID that identifies the data unit extension system. This can be one of the predefined GUIDs listed in <a href="https://msdn.microsoft.com/5aede025-65ae-4615-9511-af22b8c0dc00">INSSBuffer3::SetProperty</a>, or a GUID whose value is understood by a custom player application.


### -param cbExtensionDataSize [in]

Size, in bytes, of the data unit extensions that will be attached to the packets in the stream. Set to 0xFFFF to specify data unit extensions of variable size. Each individual data unit extension can then be set to any size ranging from 0 to 65534.


### -param pbExtensionSystemInfo [in]

Pointer to a byte buffer containing information about the data unit extension system. If you have no information, you can pass <b>NULL</b>. When passing <b>NULL</b>, <i>cbExtensionSystemInfo</i> must be zero.


### -param cbExtensionSystemInfo [in]

Count of bytes in the buffer at <i>pbExtensionSystemInfo</i>. If you have no data unit extension system information, you can pass zero. When passing zero, <i>pbExtensionSystemInfo</i> must be <b>NULL</b>.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>cbExtensionSystemInfo</i> specifies a non-zero value, but <i>pbExtensionSystemInfo</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The method cannot allocate memory to hold the new data unit extension.

</td>
</tr>
</table>
 




## -remarks



Passing the GUID of an existing data unit extension system does not cause an error. The old system is destroyed and replaced by the new one.

The new value will not take effect in the profile until you call <a href="https://msdn.microsoft.com/ac6de14b-b754-4f61-9f9a-656885641fbc">IWMProfile::ReconfigStream</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/766124f6-b376-421b-b2ee-2c280af3bd16">IWMStreamConfig2::GetDataUnitExtension</a>
 

 

