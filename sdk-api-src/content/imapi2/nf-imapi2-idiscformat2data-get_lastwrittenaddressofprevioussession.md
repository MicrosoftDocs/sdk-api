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

# IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession


## -description


Retrieves the last sector of the previous write session.


## -parameters




### -param value [out]

  Address where the previous write operation ended.  

The value is -1 if the media is blank or does not support multi-session writing (indicates that no previous session could be detected).


## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>
 




## -remarks



<div class="alert"><b>Note</b>  This property should not be used. Instead, you should use an interface derived from <a href="https://msdn.microsoft.com/a983af02-ee0e-4a62-8ae0-fb9a1e0c2571">IMultisession</a>, such as <a href="https://msdn.microsoft.com/b8124597-e75a-4f95-a25c-8cf59f452548">IMultisessionSequential</a>, for importing file data from the previous session.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/6bb871c2-1a6e-4cf6-94e1-7a566ce7a88e">IDiscFormat2Data</a>



<a href="https://msdn.microsoft.com/bdbab74c-80bd-4dca-8d64-6d30452a5876">IDiscFormat2Data::get_NextWritableAddress</a>



<a href="https://msdn.microsoft.com/a2f75240-9334-42a3-82d6-5ce9ddf1f3a2">IDiscFormat2Data::get_StartAddressOfPreviousSession</a>
 

 

