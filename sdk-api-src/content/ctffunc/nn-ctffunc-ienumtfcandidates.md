---
UID: NN:ctffunc.IEnumTfCandidates
title: IEnumTfCandidates
author: windows-sdk-content
description: The IEnumTfCandidates interface is implemented by a text service and used by the TSF manager to provide an enumeration of candidate string objects.
old-location: tsf\ienumtfcandidates.htm
tech.root: TSF
ms.assetid: 4daef7e9-e5ab-4eb8-acb6-a475b84d4de6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IEnumTfCandidates, IEnumTfCandidates interface [Text Services Framework], IEnumTfCandidates interface [Text Services Framework],described, _tsf_ienumtfcandidates_ref, ctffunc/IEnumTfCandidates, tsf.ienumtfcandidates
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - IEnumTfCandidates
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfCandidates interface


## -description


The <b>IEnumTfCandidates</b> interface is implemented by a text service and used by the TSF manager to provide an enumeration of candidate string objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfCandidates</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IEnumTfCandidates</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IEnumTfCandidates</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538127(v=VS.85).aspx">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538129(v=VS.85).aspx">Next</a>
</td>
<td align="left" width="63%">
Obtains, from the current position, the specified number of elements in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538131(v=VS.85).aspx">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms538133(v=VS.85).aspx">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/f63799a1-2284-4da8-933c-f3616c1cb295">ITfCandidateList::EnumCandidates
      </a>



<a href="https://msdn.microsoft.com/82c77b59-a50c-42ae-ba1d-25a1c196662d">ITfCandidateString
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

