---
UID: NF:msctf.IEnumTfProperties.Clone
title: IEnumTfProperties::Clone
author: windows-driver-content
description: IEnumTfProperties::Clone method
old-location: tsf\ienumtfproperties_clone.htm
old-project: TSF
ms.assetid: ee90f452-7e50-4b9a-b81d-b5d4244f55b4
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: Clone, Clone method [Text Services Framework], Clone method [Text Services Framework],IEnumTfProperties interface, IEnumTfProperties interface [Text Services Framework],Clone method, IEnumTfProperties.Clone, IEnumTfProperties::Clone, _tsf_ienumtfproperties_clone_ref, msctf/IEnumTfProperties::Clone, tsf.ienumtfproperties_clone
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
-	IEnumTfProperties.Clone
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# IEnumTfProperties::Clone


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/99d8564f-98bc-4f30-bff9-923a4016a5fe">IEnumTfProperties</a> interface pointer that receives the new enumerator.


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
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The method is not implemented.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/99d8564f-98bc-4f30-bff9-923a4016a5fe">IEnumTfProperties
      </a>
 

 

