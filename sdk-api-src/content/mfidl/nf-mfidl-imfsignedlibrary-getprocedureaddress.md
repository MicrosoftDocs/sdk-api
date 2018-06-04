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

# IMFSignedLibrary::GetProcedureAddress


## -description


Gets the procedure address of the specified function in the signed library.


## -parameters




### -param name

The entry point name in the DLL that specifies the function.


### -param address

Receives the address of the entry point.


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



See  <a href="https://msdn.microsoft.com/979A5FE5-0DED-4C5A-A27D-CDD10A4A8D5C">MFLoadSignedLibrary</a> for an example of how to create an <a href="https://msdn.microsoft.com/1170fd74-7da4-49a8-b095-dd1572db382d">IMFSignedLibrary</a> object and call the <b>GetProcedureAddress</b> method.




## -see-also




<a href="https://msdn.microsoft.com/1170fd74-7da4-49a8-b095-dd1572db382d">IMFSignedLibrary</a>



<a href="https://msdn.microsoft.com/979A5FE5-0DED-4C5A-A27D-CDD10A4A8D5C">MFLoadSignedLibrary</a>
 

 

