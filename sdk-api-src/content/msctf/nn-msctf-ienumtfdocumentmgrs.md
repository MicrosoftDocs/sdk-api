---
UID: NN:msctf.IEnumTfDocumentMgrs
title: IEnumTfDocumentMgrs (msctf.h)
author: windows-sdk-content
description: The IEnumTfDocumentMgrs interface is implemented by the TSF manager to provide an enumeration of document manager objects.
old-location: tsf\ienumtfdocumentmgrs.htm
tech.root: TSF
ms.assetid: 5b276752-715b-4426-ad37-8658bae4c1a6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumTfDocumentMgrs, IEnumTfDocumentMgrs interface [Text Services Framework], IEnumTfDocumentMgrs interface [Text Services Framework],described, _tsf_ienumtfdocumentmgrs_ref, msctf/IEnumTfDocumentMgrs, tsf.ienumtfdocumentmgrs
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
 - IEnumTfDocumentMgrs
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# IEnumTfDocumentMgrs interface


## -description


The <b>IEnumTfDocumentMgrs</b> interface is implemented by the TSF manager to provide an enumeration of document manager objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumTfDocumentMgrs</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumTfDocumentMgrs</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumTfDocumentMgrs</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d7a6ff9c-327b-45bf-93d0-7bf08065ad9c">Clone</a>
</td>
<td align="left" width="63%">
Creates a copy of the enumerator object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2fe1beed-9952-4e6c-9c45-eb21c4918288">Next</a>
</td>
<td align="left" width="63%">
Obtains the specified number of elements in the enumeration sequence from the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f7b016d-ff67-4b73-b373-b5a04cd25b58">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumerator object by moving the current position to the beginning of the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/04464160-d171-4c83-91f0-068a1c13544a">Skip</a>
</td>
<td align="left" width="63%">
Moves the current position forward in the enumeration sequence by the specified number of elements.

</td>
</tr>
</table> 

