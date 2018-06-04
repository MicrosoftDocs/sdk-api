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

# IPropertyStore::Commit


## -description


After a change has been made, this method saves the changes.


## -parameters






#### - VOID


## -returns



The <code>IPropertyStore::Commit</code> method returns any one of the following:

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
All of the property changes were successfully written to the stream or path. This includes the case where no changes were pending when the method was called and nothing was written.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STG_E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The stream or file is read-only; the method was not able to set the value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Some or all of the changes could not be written to the file. Another, more explanatory error can be used in place of E_FAIL.

</td>
</tr>
</table>
 




## -remarks



Before the <code>Commit</code> method returns, it releases the file stream or path that was initialized to be used by the method. Therefore, no <b>IPropertyStore</b> methods succeed after <code>Commit</code> returns. At that point, they return E_FAIL.

Property handlers must ensure that property changes result in a valid destination file, even if the <code>Commit</code> process terminates abnormally, or encounters any errors.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536954">IPropertyStore</a>
 

 

