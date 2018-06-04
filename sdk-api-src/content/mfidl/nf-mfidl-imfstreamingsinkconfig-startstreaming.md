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

# IMFStreamingSinkConfig::StartStreaming


## -description


Called by the streaming media client before the Media Session starts streaming to specify the byte offset or the time offset.


## -parameters




### -param fSeekOffsetIsByteOffset [in]

    A Boolean value that specifies whether <i>qwSeekOffset</i> gives a byte offset of a time offset.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRUE"></a><a id="true"></a><dl>
<dt><b>TRUE</b></dt>
</dl>
</td>
<td width="60%">
The <i>qwSeekOffset</i> parameter specifies a byte offset.

</td>
</tr>
<tr>
<td width="40%"><a id="FALSE"></a><a id="false"></a><dl>
<dt><b>FALSE</b></dt>
</dl>
</td>
<td width="60%">
The <i>qwSeekOffset</i> parameter specifies the time position in 100-nanosecond units.

</td>
</tr>
</table>
 


### -param qwSeekOffset [in]

A byte offset or a time offset, depending on the value passed in <i>fSeekOffsetIsByteOffset</i>.  Time offsets are specified in
    100-nanosecond units.



## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/5eaef815-9660-487a-885d-457cd270ba3d">IMFStreamingSinkConfig</a>
 

 

