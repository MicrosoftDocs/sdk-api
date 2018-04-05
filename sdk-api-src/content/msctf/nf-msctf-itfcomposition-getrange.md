---
UID: NF:msctf.ITfComposition.GetRange
title: ITfComposition::GetRange method
author: windows-driver-content
description: ITfComposition::GetRange method
old-location: tsf\itfcomposition_getrange.htm
old-project: TSF
ms.assetid: 14a726c3-6531-4d49-9f22-20460be02b81
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetRange method [Text Services Framework], GetRange method [Text Services Framework], ITfComposition interface, GetRange,ITfComposition.GetRange, ITfComposition, ITfComposition interface [Text Services Framework], GetRange method, ITfComposition::GetRange, _tsf_itfcomposition_getrange_ref, msctf/ITfComposition::GetRange, tsf.itfcomposition_getrange
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
-	ITfComposition.GetRange
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfComposition::GetRange method


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




<a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfRange
      </a>
 

 

