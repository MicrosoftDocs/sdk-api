---
UID: NN:rend.IEnumDirectoryObject
title: IEnumDirectoryObject (rend.h)
author: windows-sdk-content
description: The IEnumDirectoryObject interface provides COM-standard enumeration methods for the ITDirectoryObject interface. The ITDirectory::EnumerateDirectoryObjects method returns a pointer to IEnumDirectoryObject.
old-location: tapi3\ienumdirectoryobject.htm
tech.root: Tapi
ms.assetid: 328183cd-a80b-4f1f-9e5e-9f466a4e4b43
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumDirectoryObject, IEnumDirectoryObject interface [TAPI 2.2], IEnumDirectoryObject interface [TAPI 2.2],described, _tapi3_ienumdirectoryobject, rend/IEnumDirectoryObject, tapi3.ienumdirectoryobject
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
ms.custom: 19H1
---

# IEnumDirectoryObject interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IEnumDirectoryObject</b> interface provides COM-standard enumeration methods for the 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nn-rend-itdirectoryobject">ITDirectoryObject</a> interface. The 
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-itdirectory-enumeratedirectoryobjects">ITDirectory::EnumerateDirectoryObjects</a> method returns a pointer to 
<b>IEnumDirectoryObject</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumDirectoryObject</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumDirectoryObject</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdirectoryobject-clone">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdirectoryobject-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdirectoryobject-reset">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/rend/nf-rend-ienumdirectoryobject-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.

</td>
</tr>
</table> 

