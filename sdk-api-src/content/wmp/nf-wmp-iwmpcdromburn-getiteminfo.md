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

# IWMPCdromBurn::getItemInfo


## -description



The <b>getItemInfo</b> method retrieves the value of the specified attribute for the CD.




## -parameters




### -param bstrItem [in]

<b>BSTR</b> that contains one of the following values.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>AvailableTime</td>
<td>Retrieves the time available on the CD, in seconds.</td>
</tr>
<tr>
<td>Blank</td>
<td>Retrieves a <b>Boolean</b> (represented as a string) indicating whether the CD is blank.</td>
</tr>
<tr>
<td>FreeSpace</td>
<td>Retrieves the free space on the CD, in bytes.</td>
</tr>
<tr>
<td>TotalSpace</td>
<td>Retrieves the total space on the CD, in bytes.</td>
</tr>
</table>
 


### -param pbstrVal [out]

Pointer to a <b>BSTR</b> that receives the returned value.


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



<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>
 

 

