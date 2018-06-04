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

# IWindowsDriverUpdate2::CopyToCache


## -description


Copies the external update binaries  to an update.


## -parameters




### -param pFiles [in]

An <a href="https://msdn.microsoft.com/3aaab669-1f80-41ee-8c29-6da613ebccff">IStringCollection</a> interface that contains the strings to be copied to an update.


#### - ignoreDigests [in]

If the value of the <i>ignoreDigests</i> parameter is <b>VARIANT_TRUE</b>, Windows Update Agent (WUA) ignores the digest mismatches when WUA copies from the location represented by the <i>pFiles</i> parameter.


If the value of <i>ignoreDigests</i> is <b>VARIANT_FALSE</b>, WUA does not ignore the digest mismatches when WUA copies from the location represented by the <i>pFiles</i> parameter.


## -returns



Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows error code. 

This method can also return the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
This  method cannot be called from a remote computer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A parameter value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer could not access the update site.

</td>
</tr>
</table>
 




## -remarks



This method returns <b>WU_E_INVALID_OPERATION</b> if the object that is  implementing the interface has been locked down.




## -see-also




<a href="https://msdn.microsoft.com/9a2d6318-c5f0-41bc-a4df-bb9a53c9dee4">IWindowsDriverUpdate2</a>
 

 

