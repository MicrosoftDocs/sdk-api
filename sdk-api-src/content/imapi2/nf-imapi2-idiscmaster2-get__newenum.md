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

# IDiscMaster2::get__NewEnum


## -description


Retrieves a list of the CD and DVD devices installed on the computer.


## -parameters




### -param ppunk [out]

An <b>IEnumVariant</b> interface that you use to enumerate the CD and DVD devices installed on the computer. The items of the enumeration are variants whose type is <b>VT_BSTR</b>. Use the <b>bstrVal</b> member to retrieve the unique identifier of the device.


## -returns



S_OK is returned when the number of requested elements (<i>celt</i>) are returned successfully or the number of returned items (<i>pceltFetched</i>) is less than the number of requested elements. The <i>celt</i> and <i>pceltFetched</i> parameters are defined by <b>IEnumVariant</b>.

Other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>
 




## -remarks



The enumeration is a snapshot of the devices on the computer at the time of the call and will not reflect devices that are added and removed. To receive notification when a device is added or removed from the computer, implement the <a href="https://msdn.microsoft.com/f01fa2d8-989d-499f-b79d-495108640aa2">DDiscMaster2Events</a> interface.

To retrieve a single identifier, see the <a href="https://msdn.microsoft.com/e909acb9-850b-404d-a2f7-efb37faf3506">IDiscMaster2::get_Item</a> property.

The device identifier is guaranteed to be unique and static for a given device as recognized by Windows Plug and Play.  You can use the identifier as a key value for saving the user's default burner, and can also be used to cache other device-specific static information (for example, VendorID and ProductID) by an advanced application.




## -see-also




<a href="https://msdn.microsoft.com/cdca44d4-6ab5-4c2f-91ba-bef79b1d457e">IDiscMaster2</a>



<a href="https://msdn.microsoft.com/b1e0ec8f-4c66-4648-ad76-2998200ea574">IDiscMaster2::get_Count</a>
 

 

