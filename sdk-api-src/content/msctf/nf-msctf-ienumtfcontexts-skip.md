---
UID: NF:msctf.IEnumTfContexts.Skip
title: IEnumTfContexts::Skip (msctf.h)
author: windows-sdk-content
description: IEnumTfContexts::Skip method
old-location: tsf\ienumtfcontexts_skip.htm
tech.root: TSF
ms.assetid: 68f0c073-0ba5-4a46-a459-b213145aebd6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumTfContexts interface [Text Services Framework],Skip method, IEnumTfContexts.Skip, IEnumTfContexts::Skip, Skip, Skip method [Text Services Framework], Skip method [Text Services Framework],IEnumTfContexts interface, _tsf_ienumtfcontexts_skip_ref, msctf/IEnumTfContexts::Skip, tsf.ienumtfcontexts_skip
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
 - IEnumTfContexts.Skip
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfContexts::Skip


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
 



