---
UID: NF:msctf.IEnumITfCompositionView.Clone
title: IEnumITfCompositionView::Clone
author: windows-sdk-content
description: IEnumITfCompositionView::Clone method
old-location: tsf\ienumitfcompositionview_clone.htm
old-project: TSF
ms.assetid: 536b89ee-c2bd-4713-aa2c-2a2e4841a8de
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumITfCompositionView interface, IEnumITfCompositionView interface [Text Services Framework],Clone method, IEnumITfCompositionView.Clone, IEnumITfCompositionView::Clone, _tsf_ienumitfcompositionview_clone_ref, msctf/IEnumITfCompositionView::Clone, tsf.ienumitfcompositionview_clone
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
 - msctf.dll
api_name:
 - IEnumITfCompositionView.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumITfCompositionView::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/d842b367-a605-4ed0-887d-89dfcf6893a6">IEnumITfCompositionView</a> interface pointer that receives the new enumerator.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d842b367-a605-4ed0-887d-89dfcf6893a6">IEnumITfCompositionView
      </a>
 

 

