---
UID: NF:rend.ITDirectory.get_DirectoryObjects
title: ITDirectory::get_DirectoryObjects
author: windows-driver-content
description: The get_DirectoryObjects method gets the collection of objects in a given directory that matches certain criteria. This method performs the same function as EnumerateDirectoryObjects but is used by Visual Basic and other scripting languages.
old-location: tapi3\itdirectory_get_directoryobjects.htm
old-project: Tapi
ms.assetid: dd768103-4dfc-4be2-accf-38e33959102d
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: ITDirectory interface [TAPI 2.2],get_DirectoryObjects method, ITDirectory.get_DirectoryObjects, ITDirectory::get_DirectoryObjects, _tapi3_itdirectory_get_directoryobjects, get_DirectoryObjects, get_DirectoryObjects method [TAPI 2.2], get_DirectoryObjects method [TAPI 2.2],ITDirectory interface, rend/ITDirectory::get_DirectoryObjects, tapi3.itdirectory_get_directoryobjects
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rend.h
req.include-header: 
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
req.typenames: RND_ADVERTISING_SCOPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Rend.dll
api_name:
-	ITDirectory.get_DirectoryObjects
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ITDirectory::get_DirectoryObjects


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>get_DirectoryObjects</b> method gets the collection of objects in a given directory that matches certain criteria. This method performs the same function as 
<a href="https://msdn.microsoft.com/4d7e0fd5-b85b-41e0-9603-132243a9a265">EnumerateDirectoryObjects</a> but is used by Visual Basic and other scripting languages.


## -parameters




### -param DirectoryObjectType [in]

The 
<a href="https://msdn.microsoft.com/17deac23-a81f-4bb3-a6e5-4105c504c0b5">DIRECTORY_OBJECT_TYPE</a> criteria for object desired.


### -param pName [in]

Pointer to a <b>BSTR</b> containing the full or partial name of the object. The "*" wildcard is supported.


### -param pVariant [out]

Pointer to a <b>VARIANT</b> that receives an 
<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a> of 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a> objects in the server that match the description.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
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
<dt><b>RND_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="https://msdn.microsoft.com/b781008b-430a-444e-a700-8cde09e721b4">ITDirectory::Connect</a> method has not been invoked or did not succeed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not implemented.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="9e0437a2-9b4a-4576-88b0-5cb9d08ca29b">SysAllocString</a> to allocate memory for the <i>pName</i> parameter and use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory when the variable is no longer needed.

TAPI calls the <b>AddRef</b> method on the 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a> interface returned by <b>ITDirectory::get_DirectoryObjects</b>. The application must call <b>Release</b> on the 
<b>ITDirectoryObject</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/17deac23-a81f-4bb3-a6e5-4105c504c0b5">DIRECTORY_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/2286678a-68b9-4f4a-b36b-7fdf8cdad6a6">ITCollection</a>



<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>



<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a>
 

 

