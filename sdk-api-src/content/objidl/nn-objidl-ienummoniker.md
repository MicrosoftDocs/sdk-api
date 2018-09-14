---
UID: NN:objidl.IEnumMoniker
title: IEnumMoniker
author: windows-sdk-content
description: Enumerates the components of a moniker or the monikers in a table of monikers.
old-location: com\ienummoniker.htm
tech.root: com
ms.assetid: c8dec22b-946d-48ae-9315-54d353f3b853
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: IEnumMoniker, IEnumMoniker interface [COM], IEnumMoniker interface [COM],described, _ole_ienummoniker, com.ienummoniker, objidl/IEnumMoniker
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - ObjIdl.h
api_name:
 - IEnumMoniker
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumMoniker interface


## -description


Enumerates the components of a moniker or the monikers in a table of monikers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumMoniker</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IEnumMoniker</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumMoniker</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6238e556-9ef4-42c7-95ba-12468cec6b52">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ab4fd626-bddc-42b4-b279-b89d1f79b1e1">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b7c74b4-cbcb-44cc-8bea-feb55abb5643">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90df5bc4-6bb0-44bf-b675-d4a93d4680ce">Skip</a>
</td>
<td align="left" width="63%">
Skips over the specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7e2e4d92-d5dd-4294-944e-8b1e88901ee1">IMoniker::Enum</a>



<a href="https://msdn.microsoft.com/09ff0d05-627b-4e47-8534-25cd8735c6e5">IRunningObjectTable::EnumRunning</a>
 

 

