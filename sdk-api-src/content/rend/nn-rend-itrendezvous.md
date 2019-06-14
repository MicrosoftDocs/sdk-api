---
UID: NN:rend.ITRendezvous
title: ITRendezvous (rend.h)
author: windows-sdk-content
description: The ITRendezvous interface is the main interface for the Rendezvous control. An application calls the COM CoCreateInstance function on this interface to create the Rendezvous object.
old-location: tapi3\itrendezvous.htm
tech.root: Tapi
ms.assetid: ea8b0a66-b968-4a24-95db-e702d49a2870
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITRendezvous, ITRendezvous interface [TAPI 2.2], ITRendezvous interface [TAPI 2.2],described, _tapi3_itrendezvous, rend/ITRendezvous, tapi3.itrendezvous
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
 - ITRendezvous
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITRendezvous interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>ITRendezvous</b> interface is the main interface for the Rendezvous control. An application calls the COM 
<a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> function on this interface to create the Rendezvous object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITRendezvous</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITRendezvous</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itrendezvous-createdirectory">CreateDirectory</a>
</td>
<td align="left" width="63%">
Creates a directory of given type and name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itrendezvous-createdirectoryobject">CreateDirectoryObject</a>
</td>
<td align="left" width="63%">
Creates a new directory object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itrendezvous-enumeratedefaultdirectories">EnumerateDefaultDirectories</a>
</td>
<td align="left" width="63%">
Enumerates default directories.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itrendezvous-get_defaultdirectories">get_DefaultDirectories</a>
</td>
<td align="left" width="63%">
Gets the default directories configured by the system administrator. Similar to 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itrendezvous-enumeratedefaultdirectories">EnumerateDefaultDirectories</a> but used by Visual Basic and other scripting languages.

</td>
</tr>
</table> 

