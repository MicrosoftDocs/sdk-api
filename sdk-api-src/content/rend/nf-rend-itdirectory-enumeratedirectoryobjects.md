---
UID: NF:rend.ITDirectory.EnumerateDirectoryObjects
title: ITDirectory::EnumerateDirectoryObjects
author: windows-sdk-content
description: The EnumerateDirectoryObjects method creates an enumeration of directory objects of a given type and name.
old-location: tapi3\itdirectory_enumeratedirectoryobjects.htm
old-project: tapi
ms.assetid: 4d7e0fd5-b85b-41e0-9603-132243a9a265
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: EnumerateDirectoryObjects, EnumerateDirectoryObjects method [TAPI 2.2], EnumerateDirectoryObjects method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],EnumerateDirectoryObjects method, ITDirectory.EnumerateDirectoryObjects, ITDirectory::EnumerateDirectoryObjects, _tapi3_itdirectory_enumeratedirectoryobjects, rend/ITDirectory::EnumerateDirectoryObjects, tapi3.itdirectory_enumeratedirectoryobjects
ms.prod: windows
ms.technology: windows-sdk
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
 - ITDirectory.EnumerateDirectoryObjects
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# ITDirectory::EnumerateDirectoryObjects


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>EnumerateDirectoryObjects</b> method creates an enumeration of directory objects of a given type and name.


## -parameters




### -param DirectoryObjectType [in]

The 
<a href="https://msdn.microsoft.com/17deac23-a81f-4bb3-a6e5-4105c504c0b5">DIRECTORY_OBJECT_TYPE</a> criteria for object desired.


### -param pName [in]

Pointer to a <b>BSTR</b> containing the full or partial name of the object. The "*" wildcard is supported.


### -param ppEnumObject [out]

Pointer to receive 
<a href="https://msdn.microsoft.com/328183cd-a80b-4f1f-9e5e-9f466a4e4b43">IEnumDirectoryObject</a> interface pointer for the enumerator of matching objects.


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
<a href="https://msdn.microsoft.com/328183cd-a80b-4f1f-9e5e-9f466a4e4b43">IEnumDirectoryObject</a> interface returned by <b>ITDirectory::EnumerateDirectoryObjects</b>. The application must call <b>Release</b> on the 
<b>IEnumDirectoryObject</b> interface to free resources associated with it.




## -see-also




<a href="https://msdn.microsoft.com/17deac23-a81f-4bb3-a6e5-4105c504c0b5">DIRECTORY_OBJECT_TYPE</a>



<a href="https://msdn.microsoft.com/328183cd-a80b-4f1f-9e5e-9f466a4e4b43">IEnumDirectoryObject</a>



<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>
 

 

