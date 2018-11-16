---
UID: NF:msctf.ITfComposition.EndComposition
title: ITfComposition::EndComposition
author: windows-sdk-content
description: ITfComposition::EndComposition method
old-location: tsf\itfcomposition_endcomposition.htm
tech.root: TSF
ms.assetid: b5717c03-2611-4199-b07d-b6f3b6f65d3a
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: EndComposition, EndComposition method [Text Services Framework], EndComposition method [Text Services Framework],ITfComposition interface, ITfComposition interface [Text Services Framework],EndComposition method, ITfComposition.EndComposition, ITfComposition::EndComposition, _tsf_itfcomposition_endcomposition_ref, msctf/ITfComposition::EndComposition, tsf.itfcomposition_endcomposition
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
 - ITfComposition.EndComposition
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfComposition.EndComposition
: 
---

# ITfComposition::EndComposition


## -description




## -parameters




### -param ecWrite [in]

Contains an edit cookie that identifies the edit context obtained from <a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession</a>.


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
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
This value results when:

<ul>
<li>The composition terminated.</li>
<li>The caller is inside another composition write operation.</li>
<li>The caller does not own the composition.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TF_E_NOLOCK</b></dt>
</dl>
</td>
<td width="60%">
The edit context identified by <i>ecWrite</i> does not have a read/write lock.

</td>
</tr>
</table>
 




## -remarks



This method does not release the composition object, but the <a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfComposition</a> methods will fail with E_UNEXPECTED after this method is called.

Context owners should use the <a href="https://msdn.microsoft.com/950ba2b3-cb12-4697-a4b2-1c87373b9a23">ITFContextOwnerCompositionServices::TerminateComposition</a> method to terminate a composition.

This method causes the GUID_PROP_COMPOSING property to be removed from the text covered by the composition.




## -see-also




<a href="https://msdn.microsoft.com/950ba2b3-cb12-4697-a4b2-1c87373b9a23">ITFContextOwnerCompositionServices::TerminateComposition
      </a>



<a href="https://msdn.microsoft.com/b1eb5782-13e3-4cbb-8c37-ce7219d1e838">ITfComposition
      </a>



<a href="https://msdn.microsoft.com/f89b2676-9a69-492f-be8a-96e4436d594c">ITfEditSession::DoEditSession
      </a>
 

 

