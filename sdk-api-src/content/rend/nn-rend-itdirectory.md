---
UID: NN:rend.ITDirectory
title: ITDirectory (rend.h)
description: The ITDirectory interface is exposed by the Directory object, which corresponds to a particular directory.
helpviewer_keywords: ["ITDirectory","ITDirectory interface [TAPI 2.2]","ITDirectory interface [TAPI 2.2]","described","_tapi3_itdirectory","rend/ITDirectory","tapi3.itdirectory"]
old-location: tapi3\itdirectory.htm
tech.root: Tapi
ms.assetid: 9ec8c0ed-2fed-4701-acb5-86b69c10f18c
ms.date: 12/05/2018
ms.keywords: ITDirectory, ITDirectory interface [TAPI 2.2], ITDirectory interface [TAPI 2.2],described, _tapi3_itdirectory, rend/ITDirectory, tapi3.itdirectory
f1_keywords:
- rend/ITDirectory
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
- ITDirectory
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITDirectory interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITDirectory</b> interface is exposed by the Directory object, which corresponds to a particular directory. This interface provides methods that get and set directory information, and provide access to a particular directory object, such a conference or user. The 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itrendezvous-createdirectory">ITRendezvous::CreateDirectory</a> and 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdirectory-next">IEnumDirectory::Next</a> methods create the 
<b>ITDirectory</b> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITDirectory</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITDirectory</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-adddirectoryobject">AddDirectoryObject</a>
</td>
<td align="left" width="63%">
Adds an object to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-bind">Bind</a>
</td>
<td align="left" width="63%">
Binds to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-connect">Connect</a>
</td>
<td align="left" width="63%">
Connects to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-deletedirectoryobject">DeleteDirectoryObject</a>
</td>
<td align="left" width="63%">
Deletes an object from the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-enableautorefresh">EnableAutoRefresh</a>
</td>
<td align="left" width="63%">
Enables the auto refresh for the objects created afterward.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-enumeratedirectoryobjects">EnumerateDirectoryObjects</a>
</td>
<td align="left" width="63%">
Creates an enumeration of directory objects of a given type and name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-get_defaultobjectttl">get_DefaultObjectTTL</a>
</td>
<td align="left" width="63%">
Gets the default 
<a href="/windows/win32/tapi/t-tapgloss">time to live</a> (TTL) for the objects created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-get_directoryobjects">get_DirectoryObjects</a>
</td>
<td align="left" width="63%">
Gets all directory objects on the server with a specified type and name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-get_directorytype">get_DirectoryType</a>
</td>
<td align="left" width="63%">
Gets the type of the directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-get_displayname">get_DisplayName</a>
</td>
<td align="left" width="63%">
Gets the displayable name for the directory.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-get_isdynamic">get_IsDynamic</a>
</td>
<td align="left" width="63%">
Gets an indicator of whether the object on the server needs to be refreshed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-modifydirectoryobject">ModifyDirectoryObject</a>
</td>
<td align="left" width="63%">
Commits directory modifications to the server.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-put_defaultobjectttl">put_DefaultObjectTTL</a>
</td>
<td align="left" width="63%">
Sets the default TTL for the objects created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-refreshdirectoryobject">RefreshDirectoryObject</a>
</td>
<td align="left" width="63%">
Refreshes the TTL for an object on the server.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Tapi/directory-controls">Directory Controls</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

