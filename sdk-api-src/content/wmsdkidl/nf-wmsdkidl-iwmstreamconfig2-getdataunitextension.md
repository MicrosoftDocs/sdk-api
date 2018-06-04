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

# IWMStreamConfig2::GetDataUnitExtension


## -description



The <b>GetDataUnitExtension</b> method retrieves information about an existing data unit extension system.




## -parameters




### -param wDataUnitExtensionNumber [in]

<b>WORD</b> containing the data unit extension number. This number is assigned to a data unit extension system when it is added to the stream.


### -param pguidExtensionSystemID [out]

Pointer to a GUID that receives the identifier of the data unit extension system.


### -param pcbExtensionDataSize [out]

Pointer to the size, in bytes, of the data unit extensions that will be attached to the packets in the stream.

If this value is 0xFFFF, the system uses data unit extensions of variable size. Each individual data unit extension can then be set to any size ranging from 0 to 65534.


### -param pbExtensionSystemInfo [out]

Pointer to a byte buffer that receives information about the data unit extension system.


### -param pcbExtensionSystemInfo [in, out]

Pointer to the size, in bytes, of the data stored at <i>pbExtensionSystemInfo</i>.


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
<i>pguidExtensionSystemID</i> or <i>pcbExtensionDataSize</i> is <b>NULL</b>.

OR

<i>wDataUnitExtensionNumber</i> specifies an invalid data unit extension number.

</td>
</tr>
</table>
 




## -remarks



To retrieve the total number of data unit extension systems associated with the stream, call <a href="https://msdn.microsoft.com/f9a4ec84-4ea3-4e84-9def-7ca93be0f1ce">GetDataUnitExtensionCount</a>.




## -see-also




<a href="https://msdn.microsoft.com/3ce92541-6634-4418-a7ee-f9bcaf8f42ad">IWMStreamConfig2 Interface</a>



<a href="https://msdn.microsoft.com/db84a33c-bd83-46cb-a97c-76ddeeb74927">IWMStreamConfig2::AddDataUnitExtension</a>
 

 

