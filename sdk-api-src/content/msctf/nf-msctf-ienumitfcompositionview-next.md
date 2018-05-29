---
UID: NF:msctf.IEnumITfCompositionView.Next
title: IEnumITfCompositionView::Next
author: windows-sdk-content
description: IEnumITfCompositionView::Next method
old-location: tsf\ienumitfcompositionview_next.htm
old-project: TSF
ms.assetid: 70b0dd55-41c0-4188-b79e-e49a0e203949
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: IEnumITfCompositionView interface [Text Services Framework],Next method, IEnumITfCompositionView.Next, IEnumITfCompositionView::Next, Next, Next method [Text Services Framework], Next method [Text Services Framework],IEnumITfCompositionView interface, _tsf_ienumitfcompositionview_next_ref, msctf/IEnumITfCompositionView::Next, tsf.ienumitfcompositionview_next
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	IEnumITfCompositionView.Next
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumITfCompositionView::Next


## -description




## -parameters




### -param ulCount [in]

Specifies the number of elements to obtain.


### -param rgCompositionView [out]

Pointer to an array of <a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView</a> interface pointers that receives the requested objects. This array must be at least <i>ulCount</i> elements in size.


### -param pcFetched [out]

Pointer to a ULONG value that receives the number of elements obtained. This value can be less than the number of items requested. This parameter can be <b>NULL</b>.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The method reached the end of the enumeration before the specified number of elements could be obtained.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>rgCompositionView</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/d842b367-a605-4ed0-887d-89dfcf6893a6">IEnumITfCompositionView</a>



<a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView
      </a>
 

 

