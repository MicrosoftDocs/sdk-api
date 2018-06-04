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

# IWSDInboundAttachment::Close


## -description


Closes the current attachment MIME data stream.


## -parameters






## -returns



This method can return one of these values.


Possible return values include, but are not limited to, the following.



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
Method completed successfully.

</td>
</tr>
</table>
 




## -remarks



This method can be used to terminate the transfer of an incoming attachment while the transfer is in progress. 

Usually, <b>Close</b> must be called before calling <b>Release()</b> on the <a href="https://msdn.microsoft.com/1bacbf20-2eb2-4aa1-ba37-e14dc0d955b0">IWSDInboundAttachment</a>  interface. The only time a <b>Close</b> call is not required is when <a href="https://msdn.microsoft.com/library/windows/hardware/hh439702">Read</a> returns S_FALSE, which indicates that the end of the attachment stream has been reached. In that case, simply call  <b>Release()</b> on the <b>IWSDInboundAttachment</b>  interface.




## -see-also




<a href="https://msdn.microsoft.com/1bacbf20-2eb2-4aa1-ba37-e14dc0d955b0">IWSDInboundAttachment</a>
 

 

