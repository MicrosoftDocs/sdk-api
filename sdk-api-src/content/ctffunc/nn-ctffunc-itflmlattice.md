---
UID: NN:ctffunc.ITfLMLattice
title: ITfLMLattice
author: windows-sdk-content
description: The ITfLMLattice interface is implemented by the speech text service to provide information about lattice element properties and is used by a client (application or other text service).
old-location: tsf\itflmlattice.htm
tech.root: TSF
ms.assetid: 25ad6ef2-1d42-498a-852f-163a0efbc26a
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ITfLMLattice, ITfLMLattice interface [Text Services Framework], ITfLMLattice interface [Text Services Framework],described, _tsf_itflmlattice_ref, ctffunc/ITfLMLattice, tsf.itflmlattice
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - ITfLMLattice
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLMLattice interface


## -description


The <b>ITfLMLattice</b> interface is implemented by the speech text service to provide information about lattice element properties and is used by a client (application or other text service). A client obtains this interface from the GUID_PROP_LMLATTICE property by calling <a href="https://msdn.microsoft.com/c82ef360-e0b1-4e1a-b839-36b8e9c52347">ITfReadOnlyProperty::GetValue</a>. For more information, see <a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">Predefined Properties</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfLMLattice</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfLMLattice</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfLMLattice</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c42ad69f-d27a-40b7-8d63-3b422cb69db5">EnumLatticeElements</a>
</td>
<td align="left" width="63%">
Obtains an enumerator that contains all lattice elements contained in the lattice property that start at or after a specific offset from the start of the frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/199032f7-b97f-4475-9ce3-9af952e13f12">QueryType</a>
</td>
<td align="left" width="63%">
Determines if a specific lattice element type is supported by the lattice property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c82ef360-e0b1-4e1a-b839-36b8e9c52347">ITfReadOnlyProperty::GetValue
      </a>



<a href="_COM_IUnknown">IUnknown</a>



<a href="https://msdn.microsoft.com/d88f2eba-4c98-4b32-96e1-cd019fe0f7ad">Predefined Properties
      </a>
 

 

