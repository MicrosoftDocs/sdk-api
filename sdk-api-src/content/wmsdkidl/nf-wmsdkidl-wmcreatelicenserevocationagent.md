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

# WMCreateLicenseRevocationAgent function


## -description



The <b>WMCreateLicenseRevocationAgent</b> function creates a license revocation object.




## -parameters




### -param pCallback [in]

Address of the <b>IUnknown</b> interface of the object that implements the <a href="https://msdn.microsoft.com/7b8cdb21-96e1-4cf9-8422-72bce693afb1">IWMStatusCallback::OnStatus</a> callback method used to communicate license revocation status to the application.


### -param ppLicenseRevocationAgent [out]

Address of a variable that receives a pointer to the <a href="https://msdn.microsoft.com/4cb5beb9-72b8-46cb-8460-56455785a7a0">IWMLicenseRevocationAgent</a> interface of the newly created license revocation agent object.


## -returns



The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>
                  Return code
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>S_OK</td>
<td>The function succeeded.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>The function is unable to allocate memory for the new object.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

