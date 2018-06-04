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

# ILayoutStorage::ReLayoutDocfileOnILockBytes


## -description


Not supported.

The <b>ReLayoutDocfileOnILockBytes</b> method is not implemented.   If called, it returns  <b>STG_E_UNIMPLEMENTEDFUNCTION</b>.


## -parameters




### -param pILockBytes [in]

A pointer to the <a href="https://msdn.microsoft.com/bb2c5d0d-8dc8-4844-9a20-ef8e4def5731">ILockBytes</a> interface on the underlying byte-array object where the compound file is to be rewritten.


## -returns



This method returns the following value.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_UNIMPLEMENTEDFUNCTION</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented.

</td>
</tr>
</table>
 




## -remarks



If implemented, it would rewrite the compound file in the byte-array object specified by the caller.  It would return <b>S_OK</b> for success or one of the <b>STG_E_*</b> error codes for failure.



