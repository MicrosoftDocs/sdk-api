---
UID: NN:rend.IEnumDirectory
title: IEnumDirectory
author: windows-sdk-content
description: The IEnumDirectory interface provides COM-standard enumeration methods for the ITDirectory interface. The ITRendezvous::EnumerateDefaultDirectories method returns a pointer to IEnumDirectory.
old-location: tapi3\ienumdirectory.htm
tech.root: tapi
ms.assetid: 9c1e83c5-c718-4a3b-916d-e844a8377a29
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: IEnumDirectory, IEnumDirectory interface [TAPI 2.2], IEnumDirectory interface [TAPI 2.2],described, _tapi3_ienumdirectory, rend/IEnumDirectory, tapi3.ienumdirectory
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
 - IEnumDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumDirectory interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IEnumDirectory</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/9ec8c0ed-2fed-4701-acb5-86b69c10f18c">ITDirectory</a> interface. The 
<a href="https://msdn.microsoft.com/fe89a370-32ed-4519-bb98-9d9ea7615eb7">ITRendezvous::EnumerateDefaultDirectories</a> method returns a pointer to 
<b>IEnumDirectory</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDirectory</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumDirectory</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumDirectory</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/64aaf773-842b-42cd-83b8-587ec1042382">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/db164275-92dc-4a25-ba19-fd26415624f1">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5800978-198e-479d-8cca-5c4ac2399d5d">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45694bee-52d8-4a44-bc14-b9d03355bce1">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

