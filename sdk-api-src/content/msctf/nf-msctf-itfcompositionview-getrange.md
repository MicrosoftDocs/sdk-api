---
UID: NF:msctf.ITfCompositionView.GetRange
title: ITfCompositionView::GetRange
author: windows-sdk-content
description: ITfCompositionView::GetRange method
old-location: tsf\itfcompositionview_getrange.htm
old-project: TSF
ms.assetid: 31372688-be81-4883-9fc7-ed3f7b2f7934
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: GetRange, GetRange method [Text Services Framework], GetRange method [Text Services Framework],ITfCompositionView interface, ITfCompositionView interface [Text Services Framework],GetRange method, ITfCompositionView.GetRange, ITfCompositionView::GetRange, _tsf_itfcompositionview_getrange_ref, msctf/ITfCompositionView::GetRange, tsf.itfcompositionview_getrange
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
 - ITfCompositionView.GetRange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCompositionView::GetRange


## -description




## -parameters




### -param ppRange [out]

Pointer to an <a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfRange</a> interface pointer that receives the range object. It is possible that the range will have zero length.


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
<i>ppRange</i> is invalid.

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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The composition has already terminated.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1c8aac3e-384e-402e-aae8-11e240083603">ITfCompositionView</a>



<a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfRange
      </a>
 

 

