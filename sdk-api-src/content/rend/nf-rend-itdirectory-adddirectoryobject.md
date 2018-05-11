---
UID: NF:rend.ITDirectory.AddDirectoryObject
title: ITDirectory::AddDirectoryObject
author: windows-driver-content
description: The AddDirectoryObject method adds an ITDirectoryObject object to the server. This may be a directory or a user machine mapping.
old-location: tapi3\itdirectory_adddirectoryobject.htm
old-project: Tapi
ms.assetid: 7a379bdc-50e3-4034-ac16-d20d1b03cd35
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: AddDirectoryObject, AddDirectoryObject method [TAPI 2.2], AddDirectoryObject method [TAPI 2.2],ITDirectory interface, ITDirectory interface [TAPI 2.2],AddDirectoryObject method, ITDirectory.AddDirectoryObject, ITDirectory::AddDirectoryObject, _tapi3_itdirectory_adddirectoryobject, rend/ITDirectory::AddDirectoryObject, tapi3.itdirectory_adddirectoryobject
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
-	ITDirectory.AddDirectoryObject
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# ITDirectory::AddDirectoryObject


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>AddDirectoryObject</b> method adds an 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a> object to the server. This may be a directory or a user machine mapping.


## -parameters




### -param pDirectoryObject [in]

The object that will be added into the directory.


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
The <i>pDirectoryObject</i> parameter is not a valid pointer.

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
 




## -see-also




<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a>
 

 

