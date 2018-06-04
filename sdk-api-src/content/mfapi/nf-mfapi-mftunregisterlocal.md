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

# MFTUnregisterLocal function


## -description


Unregisters one or more Media Foundation transforms (MFTs) from the caller's process.


## -parameters




### -param pClassFactory [in]

A pointer to the <b>IClassFactory</b> interface of a class factory object. This parameter can be <b>NULL</b>.


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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32(<b>ERROR_NOT_FOUND</b>)</b></dt>
</dl>
</td>
<td width="60%">
The MFT specified by the <i>pClassFactory</i> parameter was not registered in this process.

</td>
</tr>
</table>
 




## -remarks



Use this function to unregister a local MFT that was previously registered through the <a href="https://msdn.microsoft.com/802f7083-e224-4e5c-8a35-3e93da0cbd91">MFTRegisterLocal</a> function.

If the <i>pClassFactory</i> parameter is <b>NULL</b>, all local MFTs in the process are unregistered. Otherwise, the function unregisters the MFT associated with the class factory specified by the <i>pClassFactory</i> parameter. In that case, the <i>pClassFactory</i> parameter should equal a pointer value that was previously passed to  the <a href="https://msdn.microsoft.com/802f7083-e224-4e5c-8a35-3e93da0cbd91">MFTRegisterLocal</a> function.




## -see-also




<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

