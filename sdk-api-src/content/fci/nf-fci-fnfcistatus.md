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

# FNFCISTATUS macro


## -description


The <b>FNFCISTATUS</b> macro provides the declaration for the application-defined callback function to update the user.


## -parameters




### -param fn

TBD






#### - cb1

Indicates a status specific value. Possible values include:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>statusFile0x00

</td>
<td>Size of the compressed block.</td>
</tr>
<tr>
<td>statusFolder0x01

</td>
<td>Amount of a folder copied to a cabinet thus far.</td>
</tr>
<tr>
<td>statusCabinet0x02

</td>
<td>Estimated cabinet size.</td>
</tr>
</table>
 


#### - cb2

Specifies a status specific value. Possible values include:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>statusFile0x00

</td>
<td>Size of the uncompressed block.</td>
</tr>
<tr>
<td>statusFolder0x01

</td>
<td>Total size of the folder.</td>
</tr>
<tr>
<td>statusCabinet0x02

</td>
<td>Actual cabinet size.</td>
</tr>
</table>
 


#### - pv

Pointer to an application-defined value.


#### - typeStatus

Indicates the type of status update. Possible values include:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>statusFile0x00

</td>
<td>Compressing a block into a folder.</td>
</tr>
<tr>
<td>statusFolder0x01

</td>
<td>Adding a folder to a cabinet.</td>
</tr>
<tr>
<td>statusCabinet0x02

</td>
<td>Writing out a complete cabinet.</td>
</tr>
</table>
 


## -remarks



If  <i>typeStatus</i> equals <b>statusCabinet</b> the returned value indicates the desired size for the cabinet file.  FCI updates the maximum cabinet size remaining using this returned value. This allows a client to generate multiple cabinets per disk, and have FCI limit the size accordingly.




## -see-also




<a href="https://msdn.microsoft.com/bfcea06d-2f09-405c-955c-0f56149148f2">FCICreate</a>
 

 

