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

# IDeviceTopology::GetSubunit


## -description



The <b>GetSubunit</b> method gets the subunit that is specified by a subunit number.




## -parameters




### -param nIndex [in]

The subunit number. If a device topology contains <i>n</i> subunits, the subunits are numbered from 0 to <i>n</i>– 1. To get the number of subunits in the device topology, call the <a href="https://msdn.microsoft.com/70fa57bb-56fe-4f8c-9967-10714f1cba22">IDeviceTopology::GetSubunitCount</a> method.


### -param ppSubunit [out]

Pointer to a pointer variable into which the method writes the address of the <a href="https://msdn.microsoft.com/9ec630bc-bba1-4a44-b66d-404a5221abbf">ISubunit</a> interface of the subunit object. Through this method, the caller obtains a counted reference to the interface. The caller is responsible for releasing the interface, when it is no longer needed, by calling the interface's <b>Release</b> method. If the <b>GetSubunit</b> call fails,  <i>*ppSubunit</i> is <b>NULL</b>.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>nIndex</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer <i>ppSubunit</i> is <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1b509f69-6277-40c0-a293-02afc30d464a">IDeviceTopology Interface</a>



<a href="https://msdn.microsoft.com/70fa57bb-56fe-4f8c-9967-10714f1cba22">IDeviceTopology::GetSubunitCount</a>



<a href="https://msdn.microsoft.com/9ec630bc-bba1-4a44-b66d-404a5221abbf">ISubunit Interface</a>
 

 

