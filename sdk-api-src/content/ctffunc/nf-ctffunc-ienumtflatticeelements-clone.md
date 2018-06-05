---
UID: NF:ctffunc.IEnumTfLatticeElements.Clone
title: IEnumTfLatticeElements::Clone
author: windows-sdk-content
description: IEnumTfLatticeElements::Clone method
old-location: tsf\ienumtflatticeelements_clone.htm
old-project: TSF
ms.assetid: 867fe614-d8c0-4987-b35a-bd5b175e6850
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfLatticeElements interface, IEnumTfLatticeElements interface [Text Services Framework],Clone method, IEnumTfLatticeElements.Clone, IEnumTfLatticeElements::Clone, _tsf_ienumtflatticeelements_clone_ref, ctffunc/IEnumTfLatticeElements::Clone, tsf.ienumtflatticeelements_clone
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TfIntegratableCandidateListSelectionStyle
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Sptip.dll
api_name:
-	IEnumTfLatticeElements.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: Sptip.dll
req.irql: 
---

# IEnumTfLatticeElements::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/5e36f052-a539-4020-8899-fb14c792c666">IEnumTfLatticeElements</a> interface pointer that receives the new enumerator.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e36f052-a539-4020-8899-fb14c792c666">IEnumTfLatticeElements
      </a>
 

 

