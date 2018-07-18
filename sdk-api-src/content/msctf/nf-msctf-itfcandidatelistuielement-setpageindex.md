---
UID: NF:msctf.ITfCandidateListUIElement.SetPageIndex
title: ITfCandidateListUIElement::SetPageIndex
author: windows-sdk-content
description: The ITfCandidateListUIElement::SetPageIndex method sets the page index.
old-location: tsf\itfcandidatelistuielement_setpageindex.htm
old-project: TSF
ms.assetid: 2e7a5185-2e4b-4f8e-b7c0-d9462d61b113
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfCandidateListUIElement interface [Text Services Framework],SetPageIndex method, ITfCandidateListUIElement.SetPageIndex, ITfCandidateListUIElement::SetPageIndex, SetPageIndex, SetPageIndex method [Text Services Framework], SetPageIndex method [Text Services Framework],ITfCandidateListUIElement interface, msctf/ITfCandidateListUIElement::SetPageIndex, tsf.itfcandidatelistuielement_setpageindex
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfCandidateListUIElement.SetPageIndex
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCandidateListUIElement::SetPageIndex


## -description


The <b>ITfCandidateListUIElement::SetPageIndex</b> method sets the page index.


## -parameters




### -param pIndex [in]

[in] A pointer to an array of the indexes that each page starts from.


### -param uPageCnt [in]

[in] A page count. The size of the pIndex buffer.


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
One or more parameters are invalid.

</td>
</tr>
</table>
 



