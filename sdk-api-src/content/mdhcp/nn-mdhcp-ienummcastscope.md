---
UID: NN:mdhcp.IEnumMcastScope
title: IEnumMcastScope
author: windows-sdk-content
description: The IEnumMcastScope interface provides COM-standard enumeration methods for the IMcastScope interface. The IMcastAddressAllocation::EnumerateScopes method returns a pointer to IEnumMcastScope.
old-location: tapi3\ienummcastscope.htm
tech.root: tapi
ms.assetid: edc8be8e-635b-43f3-a4c1-7566e354cc3e
ms.author: windowssdkdev
ms.date: 07/31/2018
ms.keywords: IEnumMcastScope, IEnumMcastScope interface [TAPI 2.2], IEnumMcastScope interface [TAPI 2.2],described, _tapi3_ienummcastscope, mdhcp/IEnumMcastScope, tapi3.ienummcastscope
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: mdhcp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Mdhcp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mdhcp.dll
api_name:
 - IEnumMcastScope
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumMcastScope interface


## -description


<p class="CCE_Message">[Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system. The RTC Client API
provides similar functionality.]

The 
<b>IEnumMcastScope</b> interface provides COM-standard enumeration methods for the 
<a href="https://msdn.microsoft.com/b0252ac4-856e-4aa7-aa3b-37b92472e864">IMcastScope</a> interface. The 
<a href="https://msdn.microsoft.com/1845f5f9-be0e-4609-89d8-1a0ed194dd68">IMcastAddressAllocation::EnumerateScopes</a> method returns a pointer to 
<b>IEnumMcastScope</b>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumMcastScope</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumMcastScope</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumMcastScope</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/96b2a09f-8a02-471d-a738-f81a8132e0c1">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.</p> (Inherited from IEnumMcastScopes)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f7618414-c2fc-46c8-8f9d-c1ad217c8d94">Next</a>
</td>
<td align="left" width="63%">
Gets the next specified number of elements in the enumeration sequence.</p> (Inherited from IEnumMcastScopes)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/799ebbdb-b285-40a6-9fd8-39341d39bbf9">Reset</a>
</td>
<td align="left" width="63%">
Resets to the beginning of the enumeration sequence.</p> (Inherited from IEnumMcastScopes)</td>
</tr>
<tr data="inherited;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e2255e7-586b-422f-a500-a32e6a460514">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration sequence.</p> (Inherited from IEnumMcastScopes)</td>
</tr>
</table> 

