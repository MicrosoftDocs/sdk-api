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

# WMIsAvailableOffline function


## -description



The <b>WMIsAvailableOffline</b> function verifies that an ASF file can be played from a cached copy. If a user plays a file from a network location, part or all of the file may be stored in a cache. If that cached copy exists on the local machine, the user may be able to play the file without being connected to the network.




## -parameters




### -param pwszURL [in]

Wide-character <b>null</b>-terminated string containing the URL of the file to be checked.


### -param pwszLanguage [in]

Wide-character <b>null</b>-terminated string containing the RFC 1766-compliant language ID specifying which language is desired for playback. This value is only important for files that contain language-based mutual exclusion.

Set to <b>NULL</b> if all languages are acceptable.


### -param pfIsAvailableOffline [out]

Pointer to a Boolean value that is set to True if the file is available offline.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or both of the input parameters are <b>NULL</b>.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/dn938561">Functions</a>
 

 

