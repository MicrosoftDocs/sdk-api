---
UID: NF:msctf.IEnumTfContexts.Clone
title: IEnumTfContexts::Clone
author: windows-sdk-content
description: IEnumTfContexts::Clone method
old-location: tsf\ienumtfcontexts_clone.htm
tech.root: TSF
ms.assetid: 9e9486b7-5251-41b9-b36c-36a0d6dfaf5d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfContexts interface, IEnumTfContexts interface [Text Services Framework],Clone method, IEnumTfContexts.Clone, IEnumTfContexts::Clone, _tsf_ienumtfcontexts_clone_ref, msctf/IEnumTfContexts::Clone, tsf.ienumtfcontexts_clone
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
 - IEnumTfContexts.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfContexts::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/20b342e6-cac4-4bc5-820b-e397e0ce4648">IEnumTfContexts</a> interface pointer that receives the new enumerator.


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




<a href="https://msdn.microsoft.com/20b342e6-cac4-4bc5-820b-e397e0ce4648">IEnumTfContexts
      </a>
 

 

