---
UID: NF:ctffunc.ITfLMLattice.EnumLatticeElements
title: ITfLMLattice::EnumLatticeElements
author: windows-driver-content
description: ITfLMLattice::EnumLatticeElements method
old-location: tsf\itflmlattice_enumlatticeelements.htm
old-project: TSF
ms.assetid: c42ad69f-d27a-40b7-8d63-3b422cb69db5
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: EnumLatticeElements, EnumLatticeElements method [Text Services Framework], EnumLatticeElements method [Text Services Framework],ITfLMLattice interface, ITfLMLattice interface [Text Services Framework],EnumLatticeElements method, ITfLMLattice.EnumLatticeElements, ITfLMLattice::EnumLatticeElements, _tsf_itflmlattice_enumlatticeelements_ref, ctffunc/ITfLMLattice::EnumLatticeElements, tsf.itflmlattice_enumlatticeelements
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfLMLattice.EnumLatticeElements
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLMLattice::EnumLatticeElements


## -description




## -parameters




### -param dwFrameStart [in]

Specifies the offset, in 100-nanosecond units, relative to the start of the phrase, of the first element to obtain.


### -param rguidType [in]

Specifies the lattice type identifier. This can be one of the <a href="https://msdn.microsoft.com/ce4bf11b-e7e7-4f06-b572-8ed6f0ed8d36">Lattice Type</a> values.


### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/5e36f052-a539-4020-8899-fb14c792c666">IEnumTfLatticeElements</a> interface pointer that receives the enumerator object.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>rguidType</i> is unsupported by the lattice property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e36f052-a539-4020-8899-fb14c792c666">
        IEnumTfLatticeElements
      </a>



<a href="https://msdn.microsoft.com/25ad6ef2-1d42-498a-852f-163a0efbc26a">ITfLMLattice</a>



<a href="https://msdn.microsoft.com/ce4bf11b-e7e7-4f06-b572-8ed6f0ed8d36">Lattice Types
      </a>
 

 

