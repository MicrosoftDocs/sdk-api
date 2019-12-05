---
UID: NN:rend.ITDirectoryObject
title: ITDirectoryObject (rend.h)
description: The ITDirectoryObject interface is the common interface supported by all objects that can be added and deleted by using the ITDirectory interface.
old-location: tapi3\itdirectoryobject.htm
tech.root: Tapi
ms.assetid: a48644a4-43e2-4c52-84be-0cb5c49e6436
ms.date: 12/05/2018
ms.keywords: ITDirectoryObject, ITDirectoryObject interface [TAPI 2.2], ITDirectoryObject interface [TAPI 2.2],described, _tapi3_itdirectoryobject, rend/ITDirectoryObject, tapi3.itdirectoryobject
ms.topic: interface
f1_keywords:
- rend/ITDirectoryObject
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITDirectoryObject interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectoryObject</b> interface is the common interface supported by all objects that can be added and deleted by using the 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectory">ITDirectory</a> interface. Changes made to this object will not take effect on the server until the 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-modifydirectoryobject">ITDirectory::ModifyDirectoryObject</a> method is called. The following methods create the 
<b>ITDirectoryObject</b> interface:


<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdirectoryobject-next">IEnumDirectoryObject::Next</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-get_directoryobjects">ITDirectory::get_DirectoryObjects</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itrendezvous-createdirectoryobject">ITRendezvous::CreateDirectoryObject</a>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDirectoryObject</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDirectoryObject</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobject-enumeratedialableaddrs">EnumerateDialableAddrs</a>
</td>
<td align="left" width="63%">
Enumerates dialable addresses.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobject-get_dialableaddrs">get_DialableAddrs</a>
</td>
<td align="left" width="63%">
Gets a dialable address for this directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobject-get_name">get_Name</a>
</td>
<td align="left" width="63%">
Gets the name of this directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobject-get_objecttype">get_ObjectType</a>
</td>
<td align="left" width="63%">
Gets the type of this directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobject-get_securitydescriptor">get_SecurityDescriptor</a>
</td>
<td align="left" width="63%">
Gets the security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobject-put_name">put_Name</a>
</td>
<td align="left" width="63%">
Sets the name of this directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectoryobject-put_securitydescriptor">put_SecurityDescriptor</a>
</td>
<td align="left" width="63%">
Sets the security descriptor.

</td>
</tr>
</table> 

