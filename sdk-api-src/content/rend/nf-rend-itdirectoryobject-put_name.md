---
UID: NF:rend.ITDirectoryObject.put_Name
title: ITDirectoryObject::put_Name
author: windows-sdk-content
description: The put_Name method sets the name of the directory object.
old-location: tapi3\itdirectoryobject_put_name.htm
old-project: tapi
ms.assetid: 398ba207-bdd7-4090-ac8b-72badbb401e3
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: ITDirectoryObject interface [TAPI 2.2],put_Name method, ITDirectoryObject.put_Name, ITDirectoryObject::put_Name, _tapi3_itdirectoryobject_put_name, put_Name, put_Name method [TAPI 2.2], put_Name method [TAPI 2.2],ITDirectoryObject interface, rend/ITDirectoryObject::put_Name, tapi3.itdirectoryobject_put_name
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rend.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rend.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RND_ADVERTISING_SCOPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectoryObject.put_Name
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# ITDirectoryObject::put_Name


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

 The 
<b>put_Name</b> method sets the name of the directory object.


## -parameters




### -param pName [in]

Pointer to <b>BSTR</b> representation of directory name.


## -returns



This method can return one of these values.

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
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>pName</i> parameter is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unspecified error.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not yet implemented.

</td>
</tr>
</table>
 




## -remarks



Changes made will not take effect on the server until the 
<a href="https://msdn.microsoft.com/be53c186-c23c-4ff6-8060-f06555ab4548">ITDirectory::ModifyDirectoryObject</a> method is called.

The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pName</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

This function may send data over the wire in unencrypted form; therefore, someone eavesdropping on the network may be able to read the data. The security risk of sending the data in clear text should be considered before using this method.




## -see-also




<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a>



<a href="https://msdn.microsoft.com/b24c1e69-5ba1-4597-86fb-2233707a1acf">ITDirectoryObject::get_Name</a>
 

 

