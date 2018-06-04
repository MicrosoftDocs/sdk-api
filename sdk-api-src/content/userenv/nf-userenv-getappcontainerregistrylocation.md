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

# GetAppContainerRegistryLocation function


## -description


Gets the location of the registry storage associated with an app container.


## -parameters




### -param desiredAccess [in]

Type: <b><a href="https://msdn.microsoft.com/003f6be9-e4ba-4d23-b486-a167063c630e">REGSAM</a></b>

The desired registry access.


### -param phAppContainerKey [out]

Type: <b>PHKEY</b>

A pointer to an HKEY that, when this function returns successfully, receives the registry storage location for the current profile.


## -returns



Type: <b>HRESULT</b>

This function returns an <b>HRESULT</b> code, including but not limited to the following:

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
The operation completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The caller is not running as or impersonating a user who can access this profile.

</td>
</tr>
</table>
 




## -remarks



The function gets the registry storage for the current user. To get the registry storage for another user, you must impersonate that user.




## -see-also




<a href="https://msdn.microsoft.com/7D3AB78D-C094-4F89-8032-13F3C137E910">GetAppContainerFolderPath</a>
 

 

