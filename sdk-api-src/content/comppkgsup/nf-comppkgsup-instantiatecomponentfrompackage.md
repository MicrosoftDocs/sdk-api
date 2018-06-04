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

# InstantiateComponentFromPackage function


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]


Creates an instance of a class in an application package. 




## -parameters




### -param classId [in]

The  class to activate in the named package.


### -param packageFullName [in]

The full name of the package.


### -param instance [out]

Receives an instance of the class.



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
<dt><b>REGDB_E_CLASSNOTREG</b></dt>
</dl>
</td>
<td width="60%">
The class is not registered or the class is not listed under the registry key "HKEY_LOCAL_MACHINE\Software\Microsoft\MediaEngine\MediaExtensions\EME\CDMS". See remarks for more info.

</td>
</tr>
</table>
 




## -remarks



This function can only be used with packages whose "PackageFamilyName"  is defined as a subkey key that is registered under the "HKEY_LOCAL_MACHINE\Software\Microsoft\MediaEngine\MediaExtensions\EME\CDMS" key. 

 This API should only be called in very exceptional circumstances because code installed from the application store should not be invoked from desktop applications as it is has a lower level of trust associated with it.



