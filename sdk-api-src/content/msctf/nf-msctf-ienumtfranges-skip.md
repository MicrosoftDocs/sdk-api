---
UID: NF:msctf.IEnumTfRanges.Skip
title: IEnumTfRanges::Skip
author: windows-sdk-content
description: IEnumTfRanges::Skip method
old-location: tsf\ienumtfranges_skip.htm
tech.root: TSF
ms.assetid: f13ec6c2-379f-42e1-af92-62c4a8d8d922
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: IEnumTfRanges interface [Text Services Framework],Skip method, IEnumTfRanges.Skip, IEnumTfRanges::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfRanges interface, _tsf_ienumtfranges_skip_ref, msctf/IEnumTfRanges::Skip, tsf.ienumtfranges_skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - IEnumTfRanges.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfRanges::Skip


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
 



