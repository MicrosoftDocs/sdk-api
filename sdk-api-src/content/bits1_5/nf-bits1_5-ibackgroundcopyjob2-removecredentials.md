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

# IBackgroundCopyJob2::RemoveCredentials


## -description


Removes credentials from use. The credentials must match an existing target and scheme pair that you specified using the 
<a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">IBackgroundCopyJob2::SetCredentials</a> method. There is no method to retrieve the credentials you have set.


## -parameters




### -param Target [in]

Identifies whether to use the credentials for proxy or server authentication.


### -param Scheme [in]

Identifies the authentication scheme to use (basic or one of several challenge-response schemes). For details, see the 
<a href="https://msdn.microsoft.com/e5a97cee-0012-4e30-850a-9adc258a36d3">BG_AUTH_SCHEME</a> enumeration.


## -returns



This method returns the following return values, as well as others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
No credentials have been set using the given <i>Target</i> and <i>Scheme</i> pair.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/e5a97cee-0012-4e30-850a-9adc258a36d3">BG_AUTH_SCHEME</a>



<a href="https://msdn.microsoft.com/efe7aa0a-48fc-4192-b81b-40d3a9b0fb22">BG_AUTH_TARGET</a>



<a href="https://msdn.microsoft.com/adaffc21-7df1-48ca-8e05-bdb09663a49b">IBackgroundCopyJob2::SetCredentials</a>
 

 

