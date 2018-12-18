---
UID: NN:oleidl.IEnumOLEVERB
title: IEnumOLEVERB
author: windows-sdk-content
description: Enumerates the different verbs available for an object in order of ascending verb number. An enumerator that implements the IEnumOLEVERB interface is returned by IOleObject::EnumVerbs.
old-location: com\ienumoleverb.htm
tech.root: com
ms.assetid: fc9b3474-6f56-4274-af7d-72e0920c0457
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumOLEVERB, IEnumOLEVERB interface [COM], IEnumOLEVERB interface [COM],described, _ole_ienumoleverb, com.ienumoleverb, oleidl/IEnumOLEVERB
ms.topic: interface
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IEnumOLEVERB
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumOLEVERB interface


## -description


Enumerates the different verbs available for an object in order of ascending verb number. An enumerator that implements the <b>IEnumOLEVERB</b> interface is returned by <a href="https://msdn.microsoft.com/c67770d0-e478-41dc-9028-1e0a6cb9e3c7">IOleObject::EnumVerbs</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOLEVERB</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IEnumOLEVERB</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumOLEVERB</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b93eafa0-c9c5-4d3f-a9a0-c5ca95df5b03">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb934017-9054-42b5-89d4-a24f12829503">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/612a364a-e7c2-4efd-b55c-1050891f5e22">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f949f993-1c4c-4d42-ba23-93330f0e9967">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 

