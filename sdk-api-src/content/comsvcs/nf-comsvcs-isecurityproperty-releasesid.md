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

# ISecurityProperty::ReleaseSID


## -description


Releases the security identifier returned by one of the other <a href="https://msdn.microsoft.com/116715a5-a3e1-48aa-b155-107ea330b7ee">ISecurityProperty</a> methods.


## -parameters




### -param pSID [in]

A reference to a security ID.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument passed in the pSid parameter is not a reference to a security ID.

</td>
</tr>
</table>
 




## -remarks



You should always invoke the <b>ReleaseSID</b> method to release any security ID pointers returned by the <a href="https://msdn.microsoft.com/e322df62-25a4-40a3-9b80-da468a265162">GetDirectCallerSID</a>, <a href="https://msdn.microsoft.com/cd06e71b-563a-45d2-91fb-f57375016dc3">GetDirectCreatorSID</a>, <a href="https://msdn.microsoft.com/e8700635-94cb-4d1a-9325-f93d00c5181f">GetOriginalCallerSID</a>, and <a href="https://msdn.microsoft.com/599b0773-feee-4e3d-a23b-cc2c294f49f9">GetOriginalCreatorSID</a> methods.




## -see-also




<a href="https://msdn.microsoft.com/9395bc9a-dfe5-428a-839f-1c4ad090f636">IObjectContext</a>



<a href="https://msdn.microsoft.com/116715a5-a3e1-48aa-b155-107ea330b7ee">ISecurityProperty</a>
 

 

