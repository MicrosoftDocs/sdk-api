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

# IMFTrustedOutput::IsFinal


## -description



Queries whether this output is a policy sink, meaning it handles the rights and restrictions required by the input trust authority (ITA).




## -parameters




### -param pfIsFinal [out]

Receives a Boolean value. If <b>TRUE</b>, this object is a policy sink. If <b>FALSE</b>, the policy must be enforced further downstream.


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



A trusted output is generally considered to be a policy sink if it does not pass the media content that it receives anywhere else; or, if it does pass the media content elsewhere, either it protects the content using some proprietary method such as encryption, or it sufficiently devalues the content so as not to require protection.




## -see-also




<a href="https://msdn.microsoft.com/14342d8b-3c76-4c13-8cbe-a60bb66084c8">IMFTrustedOutput</a>
 

 

