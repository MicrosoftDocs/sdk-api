---
UID: NN:objidl.IEnumSTATSTG
title: IEnumSTATSTG (objidl.h)
author: windows-sdk-content
description: Enumerates an array of STATSTG structures.
old-location: stg\ienumstatstg.htm
tech.root: Stg
ms.assetid: 93b8b14e-94e4-460b-9846-413affad8e4f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IEnumSTATSTG, IEnumSTATSTG interface [Structured Storage], IEnumSTATSTG interface [Structured Storage],described, _stg_ienumstatstg, objidl/IEnumSTATSTG, stg.ienumstatstg
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
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IEnumSTATSTG
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumSTATSTG interface


## -description


The 
<b>IEnumSTATSTG</b> interface enumerates an array of 
<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures. These structures contain statistical data about  open storage, stream, or byte array objects. 
<b>IEnumSTATSTG</b> has the same methods as all enumerator interfaces: <a href="https://msdn.microsoft.com/09363d3e-a606-4a50-8758-d7ef5b3c05ab">Next</a>, <a href="https://msdn.microsoft.com/97d785d9-961c-44af-a0a0-1d2f610e6c9a">Skip</a>, <a href="https://msdn.microsoft.com/696aaa93-1b56-4baf-a6be-753c7d6f5456">Reset</a>, and 
<a href="https://msdn.microsoft.com/b6bc5dbd-7e09-4590-a7d4-d58fcd297f74">Clone</a>. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumSTATSTG</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumSTATSTG</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumSTATSTG</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6bc5dbd-7e09-4590-a7d4-d58fcd297f74">Clone</a>
</td>
<td align="left" width="63%">
Creates a new enumerator that contains the same enumeration state as the current <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/09363d3e-a606-4a50-8758-d7ef5b3c05ab">Next</a>
</td>
<td align="left" width="63%">
Gets a specified number of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/696aaa93-1b56-4baf-a6be-753c7d6f5456">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning of the <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structure array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97d785d9-961c-44af-a0a0-1d2f610e6c9a">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of <a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a> structures in the enumeration sequence.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms693395(v=VS.85).aspx">CoGetMalloc</a>



<a href="https://msdn.microsoft.com/40dd62b8-f76a-4cd8-9a9f-6ac344389b6c">EnumAll Sample</a>



<a href="https://msdn.microsoft.com/29ca157e-40e2-4e9a-95fb-a31bb45570f2">IStorage::EnumElements</a>



<a href="https://msdn.microsoft.com/54e1df08-de8f-430a-bf76-e66594df4839">STATSTG</a>
 

 

