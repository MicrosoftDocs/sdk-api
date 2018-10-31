---
UID: NN:oaidl.IEnumVARIANT
title: IEnumVARIANT
author: windows-sdk-content
description: Provides a method for enumerating a collection of variants, including heterogeneous collections of objects and intrinsic types.
old-location: automat\ienumvariant.htm
tech.root: automat
ms.assetid: 139e3c93-faef-4003-9079-e0e94494db3e
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: IEnumVARIANT, IEnumVARIANT interface [Automation], IEnumVARIANT interface [Automation],described, _oa96_IEnumVARIANT_Interface, automat.ienumvariant, oaidl/IEnumVARIANT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - oaidl.h
api_name:
 - IEnumVARIANT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumVARIANT interface


## -description


Provides a method for enumerating a collection of variants, including heterogeneous collections of objects and intrinsic types. Callers of this interface do not need to know the specific type (or types) of the elements in the collection.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumVARIANT</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumVARIANT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumVARIANT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44beac4a-784d-461e-8a4b-71bdcf512fbc">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the current state of enumeration.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/691c1624-8d01-41e0-890e-a4782eba1f59">Next</a>
</td>
<td align="left" width="63%">
Retrieves the specified items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0c3f0cd7-6bad-4cb7-8b84-d8a212dbadbd">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5fe6951f-1e21-4a3d-8694-96efb15e6d11">Skip</a>
</td>
<td align="left" width="63%">
Attempts to skip over the next celt elements in the enumeration sequence.

</td>
</tr>
</table> 


## -remarks



To see how to implement a collection of objects using <b>IEnumVARIANT</b>, refer to the file Enumvar.cpp in the Lines sample code.



