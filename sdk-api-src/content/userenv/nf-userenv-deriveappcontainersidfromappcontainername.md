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

# DeriveAppContainerSidFromAppContainerName function


## -description


Gets the SID of the specified profile.


## -parameters




### -param pszAppContainerName [in]

The name of the profile.


### -param ppsidAppContainerSid [out]

The SID for the profile. This buffer must be freed using the <a href="https://msdn.microsoft.com/1e2098d8-4d1f-4353-97c1-549021a5b3fd">FreeSid</a> function.


## -returns



This function can return one of these values.

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
The <i>pszAppContainerName</i> parameter, or the  <i>ppsidAppContainerSid</i> parameter is either <b>NULL</b> or not valid.

</td>
</tr>
</table>
 



