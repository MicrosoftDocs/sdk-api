---
UID: NF:ctfutb.IEnumTfLangBarItems.Clone
title: IEnumTfLangBarItems::Clone
author: windows-sdk-content
description: IEnumTfLangBarItems::Clone method
old-location: tsf\ienumtflangbaritems_clone.htm
tech.root: TSF
ms.assetid: 2a1f4a40-cf2c-4872-bb15-c4622ab2bfd1
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfLangBarItems interface, IEnumTfLangBarItems interface [Text Services Framework],Clone method, IEnumTfLangBarItems.Clone, IEnumTfLangBarItems::Clone, _tsf_ienumtflangbaritems_clone_ref, ctfutb/IEnumTfLangBarItems::Clone, tsf.ienumtflangbaritems_clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - IEnumTfLangBarItems.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfLangBarItems::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms538185(v=VS.85).aspx">IEnumTfLangBarItems</a> interface pointer that receives the new enumerator.


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




<a href="https://msdn.microsoft.com/a3988c0f-db2d-4841-8098-f1dc133cb60a">IEnumTfLangBarItems
      </a>
 

 

