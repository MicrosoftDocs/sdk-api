---
UID: NN:rend.IEnumDirectoryObject
title: IEnumDirectoryObject
author: windows-sdk-content
description: The IEnumDirectoryObject interface provides COM-standard enumeration methods for the ITDirectoryObject interface. The ITDirectory::EnumerateDirectoryObjects method returns a pointer to IEnumDirectoryObject.
old-location: tapi3\ienumdirectoryobject.htm
tech.root: tapi
ms.assetid: 328183cd-a80b-4f1f-9e5e-9f466a4e4b43
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IEnumDirectoryObject, IEnumDirectoryObject interface [TAPI 2.2], IEnumDirectoryObject interface [TAPI 2.2],described, _tapi3_ienumdirectoryobject, rend/IEnumDirectoryObject, tapi3.ienumdirectoryobject
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
 - IEnumDirectoryObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDirectoryObject interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IEnumDirectoryObject</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/a48644a4-43e2-4c52-84be-0cb5c49e6436">ITDirectoryObject</a> interface. The 
<a href="https://msdn.microsoft.com/4d7e0fd5-b85b-41e0-9603-132243a9a265">ITDirectory::EnumerateDirectoryObjects</a> method returns a pointer to 
<b>IEnumDirectoryObject</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDirectoryObject</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumDirectoryObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDirectoryObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2be8430e-2968-416f-9503-b77d6abd6a12">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/034a704a-f5c7-46bf-a8fa-9bb6298dd4d2">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fd3d338e-f980-4a87-ae51-b59a8744d029">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e14e71f1-5151-4562-bfbf-1370f65cb23a">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

