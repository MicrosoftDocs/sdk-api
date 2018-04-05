---
UID: NF:objidl.IMoniker.Enum
title: IMoniker::Enum method
author: windows-driver-content
description: Retrieves a pointer to an enumerator for the components of a composite moniker.
old-location: com\imoniker_enum.htm
old-project: com
ms.assetid: 7e2e4d92-d5dd-4294-944e-8b1e88901ee1
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: Enum method [COM], Enum method [COM], IMoniker interface, Enum,IMoniker.Enum, IMoniker, IMoniker interface [COM], Enum method, IMoniker::Enum, _com_imoniker_enum, com.imoniker_enum, objidl/IMoniker::Enum
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ObjIdl.h
api_name:
-	IMoniker.Enum
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IMoniker::Enum method


## -description


Retrieves a pointer to an enumerator for the components of a composite moniker.


## -parameters




### -param fForward [in]

If <b>TRUE</b>, enumerates the monikers from left to right. If <b>FALSE</b>, enumerates from right to left.


### -param ppenumMoniker [out]

A pointer to an <a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a> pointer variable that receives the interface pointer to the enumerator object for the moniker. When successful, the implementation must call <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">AddRef</a> on the enumerator object. It is the caller's responsibility to call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">Release</a>. If an error occurs or if the moniker has no enumerable components, the implementation sets *<i>ppenumMoniker</i> to <b>NULL</b>.


## -returns



This method can return the standard return values E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -remarks



This method must supply an <a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a> pointer to an enumerator that can enumerate the components of a moniker. For example, the implementation of the <b>IMoniker::Enum</b> method for a generic composite moniker creates an enumerator that can determine the individual monikers that make up the composite, while the <b>IMoniker::Enum</b> method for a file moniker creates an enumerator that returns monikers representing each of the components in the path.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Call this method to examine the components that make up a composite moniker.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the new moniker class has no discernible internal structure, your implementation of this method can simply return S_OK and set <i>ppenumMoniker</i> to <b>NULL</b>.

<h3><a id="Implementation-specific_Notes"></a><a id="implementation-specific_notes"></a><a id="IMPLEMENTATION-SPECIFIC_NOTES"></a>Implementation-specific Notes</h3>
<table>
<tr>
<th>Implementation</th>
<th>Notes</th>
</tr>
<tr>
<td>Anti-moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>Class moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>File moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>Generic composite moniker</td>
<td>If successful, this method returns S_OK and passes back an enumerator that enumerates the component monikers that make up the composite; otherwise, the method returns E_OUTOFMEMORY. </td>
</tr>
<tr>
<td>Item moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>OBJREF moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
<tr>
<td>Pointer moniker</td>
<td>This method returns E_NOTIMPL.</td>
</tr>
<tr>
<td>URL moniker</td>
<td>This method returns S_OK and sets <i>ppenumMoniker</i> to <b>NULL</b>.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/c8dec22b-946d-48ae-9315-54d353f3b853">IEnumMoniker</a>



<a href="https://msdn.microsoft.com/17f4c1df-7a9c-42ef-a888-70cd8d85f070">IMoniker</a>
 

 

