---
UID: NN:rend.ITDirectory
title: ITDirectory
author: windows-sdk-content
description: The ITDirectory interface is exposed by the Directory object, which corresponds to a particular directory.
old-location: tapi3\itdirectory.htm
tech.root: Tapi
ms.assetid: 9ec8c0ed-2fed-4701-acb5-86b69c10f18c
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITDirectory, ITDirectory interface [TAPI 2.2], ITDirectory interface [TAPI 2.2],described, _tapi3_itdirectory, rend/ITDirectory, tapi3.itdirectory
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.lib: 
req.dll: Rend.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Rend.dll
api_name:
 - ITDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDirectory interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectory</b> interface is exposed by the Directory object, which corresponds to a particular directory. This interface provides methods that get and set directory information, and provide access to a particular directory object, such a conference or user. The 
<a href="https://msdn.microsoft.com/b285f852-a017-4dcd-b32e-afb2296487a5">ITRendezvous::CreateDirectory</a> and 
<a href="https://msdn.microsoft.com/db164275-92dc-4a25-ba19-fd26415624f1">IEnumDirectory::Next</a> methods create the 
<b>ITDirectory</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDirectory</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITDirectory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDirectory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7a379bdc-50e3-4034-ac16-d20d1b03cd35">AddDirectoryObject</a>
</td>
<td align="left" width="63%">
Adds an object to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4bcf994c-3091-445e-ad79-91958e48960a">Bind</a>
</td>
<td align="left" width="63%">
Binds to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b781008b-430a-444e-a700-8cde09e721b4">Connect</a>
</td>
<td align="left" width="63%">
Connects to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d2bb052-6986-4407-8a37-3a74920bf78e">DeleteDirectoryObject</a>
</td>
<td align="left" width="63%">
Deletes an object from the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4d55d7c-54b4-44ee-b8f2-f4dd51bf823d">EnableAutoRefresh</a>
</td>
<td align="left" width="63%">
Enables the auto refresh for the objects created afterward.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4d7e0fd5-b85b-41e0-9603-132243a9a265">EnumerateDirectoryObjects</a>
</td>
<td align="left" width="63%">
Creates an enumeration of directory objects of a given type and name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f0a24ad9-0020-4f62-a0f2-071b9d251f79">get_DefaultObjectTTL</a>
</td>
<td align="left" width="63%">
Gets the default 
<a href="../tapi2/t_tapgloss.htm">time to live</a> (TTL) for the objects created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd768103-4dfc-4be2-accf-38e33959102d">get_DirectoryObjects</a>
</td>
<td align="left" width="63%">
Gets all directory objects on the server with a specified type and name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f0ca4c2-4ba9-4a6e-877b-36486086368f">get_DirectoryType</a>
</td>
<td align="left" width="63%">
Gets the type of the directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a564e501-089e-41fc-9e81-bd0c9e6f951d">get_DisplayName</a>
</td>
<td align="left" width="63%">
Gets the displayable name for the directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4260ad95-d684-44e4-877f-fcdbe4fe0fd7">get_IsDynamic</a>
</td>
<td align="left" width="63%">
Gets an indicator of whether the object on the server needs to be refreshed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be53c186-c23c-4ff6-8060-f06555ab4548">ModifyDirectoryObject</a>
</td>
<td align="left" width="63%">
Commits directory modifications to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aecadd26-648e-43ce-8331-ef4af24567ed">put_DefaultObjectTTL</a>
</td>
<td align="left" width="63%">
Sets the default TTL for the objects created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85a94960-5d4e-4b23-a3ed-65743a60ee87">RefreshDirectoryObject</a>
</td>
<td align="left" width="63%">
Refreshes the TTL for an object on the server.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f5ca1d61-5266-4406-8199-338e6a712db8">Directory Controls</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

