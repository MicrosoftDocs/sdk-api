---
UID: NN:rend.ITDirectoryObject
title: ITDirectoryObject
author: windows-sdk-content
description: The ITDirectoryObject interface is the common interface supported by all objects that can be added and deleted by using the ITDirectory interface.
old-location: tapi3\itdirectoryobject.htm
tech.root: Tapi
ms.assetid: a48644a4-43e2-4c52-84be-0cb5c49e6436
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ITDirectoryObject, ITDirectoryObject interface [TAPI 2.2], ITDirectoryObject interface [TAPI 2.2],described, _tapi3_itdirectoryobject, rend/ITDirectoryObject, tapi3.itdirectoryobject
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
 - ITDirectoryObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITDirectoryObject interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectoryObject</b> interface is the common interface supported by all objects that can be added and deleted by using the 
<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a> interface. Changes made to this object will not take effect on the server until the 
<a href="https://msdn.microsoft.com/be53c186-c23c-4ff6-8060-f06555ab4548">ITDirectory::ModifyDirectoryObject</a> method is called. The following methods create the 
<b>ITDirectoryObject</b> interface:


<a href="https://msdn.microsoft.com/034a704a-f5c7-46bf-a8fa-9bb6298dd4d2">IEnumDirectoryObject::Next</a>



<a href="https://msdn.microsoft.com/dd768103-4dfc-4be2-accf-38e33959102d">ITDirectory::get_DirectoryObjects</a>



<a href="https://msdn.microsoft.com/e3ad77cf-9112-4561-896c-2eba7e07eb19">ITRendezvous::CreateDirectoryObject</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDirectoryObject</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITDirectoryObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITDirectoryObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cee7a00e-e601-47bf-b64b-61085511da97">EnumerateDialableAddrs</a>
</td>
<td align="left" width="63%">
Enumerates dialable addresses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b72e9c49-4d5a-432a-b21b-ec444912ea61">get_DialableAddrs</a>
</td>
<td align="left" width="63%">
Gets a dialable address for this directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b24c1e69-5ba1-4597-86fb-2233707a1acf">get_Name</a>
</td>
<td align="left" width="63%">
Gets the name of this directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b71f5286-d97d-4129-942b-fa4d4ef0943e">get_ObjectType</a>
</td>
<td align="left" width="63%">
Gets the type of this directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/746367e1-4319-4903-843f-7a25d60f4223">get_SecurityDescriptor</a>
</td>
<td align="left" width="63%">
Gets the security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/398ba207-bdd7-4090-ac8b-72badbb401e3">put_Name</a>
</td>
<td align="left" width="63%">
Sets the name of this directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a6fe823-c794-4b6c-af51-ef03efe62606">put_SecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor.

</td>
</tr>
</table> 

