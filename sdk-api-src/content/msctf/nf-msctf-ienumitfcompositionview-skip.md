---
UID: NF:msctf.IEnumITfCompositionView.Skip
title: IEnumITfCompositionView::Skip
author: windows-driver-content
description: IEnumITfCompositionView::Skip method
old-location: tsf\ienumitfcompositionview_skip.htm
old-project: TSF
ms.assetid: 9edc8dd8-4cbb-4250-a0e9-05d7250d5ad3
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: IEnumITfCompositionView interface [Text Services Framework],Skip method, IEnumITfCompositionView.Skip, IEnumITfCompositionView::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumITfCompositionView interface, _tsf_ienumitfcompositionview_skip_ref, msctf/IEnumITfCompositionView::Skip, tsf.ienumitfcompositionview_skip
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IEnumITfCompositionView.Skip
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumITfCompositionView::Skip


## -description




## -parameters




### -param ulCount [in]

Contains the number of elements to skip.


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
The method reached the end of the enumeration before the specified number of elements could be skipped.

</td>
</tr>
</table>
 



