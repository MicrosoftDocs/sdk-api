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

# IPortableDeviceService::Advise


## -description


The <b>Advise</b> method registers an application-defined callback object that receives service events.


## -parameters




### -param dwFlags [in]

Not used.


### -param pCallback [in]

The  <a href="https://msdn.microsoft.com/1fb2d5d8-82b8-4c51-a086-bdcad33da190">IPortableDeviceEventCallback</a> interface specifying the callback object to register.


### -param pParameters [in]

The <a href="https://msdn.microsoft.com/library/windows/hardware/ff597597">IPortableDeviceValues</a> interface specifying the event-registration parameters, or <b>NULL</b> if the callback object is to receive all service events.


### -param ppszCookie [out]

The unique context ID for the callback object. This value matches that used by the <a href="https://msdn.microsoft.com/4982efa9-82f2-457b-acf4-c6f7d48cf6f7">Unadvise</a> method to unregister the callback object.


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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> value was specified for the <i>pCallback</i> parameter or the <i>ppszCookie</i> parameter.

</td>
</tr>
</table>
 




## -remarks



During cleanup, an application should unregister the callback object by calling the <a href="https://msdn.microsoft.com/4982efa9-82f2-457b-acf4-c6f7d48cf6f7">Unadvise</a> method, and then release the memory referenced by the <i>ppszCookie</i> parameter by calling the <b>CoTaskMemFree</b> function.




## -see-also




<a href="https://msdn.microsoft.com/f57344d5-c978-4c27-b8a9-b42492bd9312">IPortableDeviceService Interface</a>
 

 

