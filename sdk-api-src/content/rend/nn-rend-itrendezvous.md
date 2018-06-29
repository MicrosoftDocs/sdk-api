---
UID: NN:rend.ITRendezvous
title: ITRendezvous
author: windows-sdk-content
description: The ITRendezvous interface is the main interface for the Rendezvous control. An application calls the COM CoCreateInstance function on this interface to create the Rendezvous object.
old-location: tapi3\itrendezvous.htm
old-project: Tapi
ms.assetid: ea8b0a66-b968-4a24-95db-e702d49a2870
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: ITRendezvous, ITRendezvous interface [TAPI 2.2], ITRendezvous interface [TAPI 2.2],described, _tapi3_itrendezvous, rend/ITRendezvous, tapi3.itrendezvous
ms.prod: windows
ms.technology: windows-sdk
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
 - ITRendezvous
product: Windows
targetos: Windows
req.lib: 
req.dll: Rend.dll
req.irql: 
req.product: ADAM
---

# ITRendezvous interface


## -description


<p class="CCE_Message">[
						Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITRendezvous</b> interface is the main interface for the Rendezvous control. An application calls the COM 
<a href="https://msdn.microsoft.com/library/ms686615(v=VS.85).aspx">CoCreateInstance</a> function on this interface to create the Rendezvous object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITRendezvous</b> interface inherits from the <a href="https://msdn.microsoft.com/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITRendezvous</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITRendezvous</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b285f852-a017-4dcd-b32e-afb2296487a5">CreateDirectory</a>
</td>
<td align="left" width="63%">
Creates a directory of given type and name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3ad77cf-9112-4561-896c-2eba7e07eb19">CreateDirectoryObject</a>
</td>
<td align="left" width="63%">
Creates a new directory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fe89a370-32ed-4519-bb98-9d9ea7615eb7">EnumerateDefaultDirectories</a>
</td>
<td align="left" width="63%">
Enumerates default directories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3db02f17-6fb5-467b-91f6-dc501b5472cf">get_DefaultDirectories</a>
</td>
<td align="left" width="63%">
Gets the default directories configured by the system administrator. Similar to 
<a href="https://msdn.microsoft.com/fe89a370-32ed-4519-bb98-9d9ea7615eb7">EnumerateDefaultDirectories</a> but used by Visual Basic and other scripting languages.

</td>
</tr>
</table> 

