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

# IDirectInputJoyConfig8::OpenAppStatusKey


## -description


The <b>IDirectInputJoyConfig8::OpenAppStatusKey </b>method opens the root key of the application status registry keys, and obtains a handle to the key as a return parameter. 


## -parameters






#### - phKey

Points to the address of a variable (of type HKEY) that will contain a registry key handle if the method succeeds. See Remarks for additional usage details.


## -returns



Returns DI_OK if successful; otherwise, returns one of the following COM error values. The following error codes are intended to be illustrative and not necessarily comprehensive.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_INVALIDPARAM</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DIERR_NOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The key is missing on this system. Applications should proceed as if the key were empty. 

</td>
</tr>
</table>
 




## -remarks



The registry key handle returned in the <i>phKey</i> parameter can be used with the standard Win32 registry functions. The Dinputd.h header file defines the following string constants for use in accessing subkeys and named values contained by the application status root key.





