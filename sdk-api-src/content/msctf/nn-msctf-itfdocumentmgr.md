---
UID: NN:msctf.ITfDocumentMgr
title: ITfDocumentMgr
author: windows-sdk-content
description: The ITfDocumentMgr interface is implemented by the TSF manager and used by an application or text service to create and manage text contexts. To obtain an instance of this interface call ITfThreadMgr::CreateDocumentMgr.
old-location: tsf\itfdocumentmgr.htm
tech.root: TSF
ms.assetid: e99e9bdb-6a3a-438d-8fac-92ef96c8dfdd
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfDocumentMgr, ITfDocumentMgr interface [Text Services Framework], ITfDocumentMgr interface [Text Services Framework],described, _tsf_itfdocumentmgr_ref, msctf/ITfDocumentMgr, tsf.itfdocumentmgr
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ITfDocumentMgr
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfDocumentMgr interface


## -description


The <b>ITfDocumentMgr</b> interface is implemented by the TSF manager and used by an application or text service to create and manage text contexts. To obtain an instance of this interface call <a href="https://msdn.microsoft.com/0f90a359-61e7-46e5-9d0b-ab6fe24f3136">ITfThreadMgr::CreateDocumentMgr</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITfDocumentMgr</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITfDocumentMgr</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITfDocumentMgr</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1415f338-731c-44c5-b798-edf823174272">CreateContext</a>
</td>
<td align="left" width="63%">
Creates a context object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0656301a-9e24-4b13-bc39-7d9085c0d6f2">EnumContexts</a>
</td>
<td align="left" width="63%">
Obtains a context enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/71248c77-7440-412c-b565-39c04108b98b">GetBase</a>
</td>
<td align="left" width="63%">
Obtains the context at the base of the context stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5be7635f-ec27-4892-9cfe-dba31e202510">GetTop</a>
</td>
<td align="left" width="63%">
Obtains the context at the top of the context stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbf65d8d-5a59-4c4b-a132-fa28babcd70b">Pop</a>
</td>
<td align="left" width="63%">
Removes the context from the top of the context stack.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/afd5452b-4121-428d-801f-1638c2767c67">Push</a>
</td>
<td align="left" width="63%">
Adds a context to the top of the context stack.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/ca98c7bb-7348-405d-976a-18012b0886c6">ITfContext
      </a>



<a href="https://msdn.microsoft.com/0f90a359-61e7-46e5-9d0b-ab6fe24f3136">ITfThreadMgr::CreateDocumentMgr
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

