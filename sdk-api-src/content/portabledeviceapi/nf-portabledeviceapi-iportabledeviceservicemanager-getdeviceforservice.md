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

# IPortableDeviceServiceManager::GetDeviceForService


## -description


The <b>GetDeviceForService</b> method retrieves the device associated with the specified service.


## -parameters




### -param pszPnPServiceID [in]

The Plug and Play (PnP) identifier of the service.


### -param ppszPnPDeviceID [out]

The retrieved PnP identifier of the device associated with the service.


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
An invalid pointer was supplied.

</td>
</tr>
</table>
 




## -remarks



Neither the <i>pszPnPServiceID</i> parameter nor the <i>pszPnPDeviceID</i> parameter can be <b>NULL</b>.

An application can retrieve a PnP service identifier by calling the <b>GetDeviceServices</b> method.




## -see-also




<a href="https://msdn.microsoft.com/8df23343-26f0-4fb0-90b9-e8b75bcadffa">IPortableDeviceServiceManager Interface</a>
 

 

