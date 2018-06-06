---
UID: NF:msctf.ITfContextComposition.EnumCompositions
title: ITfContextComposition::EnumCompositions
author: windows-sdk-content
description: ITfContextComposition::EnumCompositions method
old-location: tsf\itfcontextcomposition_enumcompositions.htm
old-project: TSF
ms.assetid: 230daf27-2655-4d67-b183-cd0f0c855298
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: EnumCompositions, EnumCompositions method [Text Services Framework], EnumCompositions method [Text Services Framework],ITfContextComposition interface, ITfContextComposition interface [Text Services Framework],EnumCompositions method, ITfContextComposition.EnumCompositions, ITfContextComposition::EnumCompositions, _tsf_itfcontextcomposition_enumcompositions_ref, msctf/ITfContextComposition::EnumCompositions, tsf.itfcontextcomposition_enumcompositions
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfContextComposition.EnumCompositions
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfContextComposition::EnumCompositions


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/d842b367-a605-4ed0-887d-89dfcf6893a6">IEnumITfCompositionView</a> interface pointer that receives the enumerator object.


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
The enumerator object could not be initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ppEnum</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The enumerator object cannot be created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_DISCONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The context object is not on a document stack.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d842b367-a605-4ed0-887d-89dfcf6893a6">IEnumITfCompositionView
      </a>



<a href="https://msdn.microsoft.com/cf02c50c-dca8-47ad-b8ff-0fa3884db674">ITfContextComposition</a>
 

 

