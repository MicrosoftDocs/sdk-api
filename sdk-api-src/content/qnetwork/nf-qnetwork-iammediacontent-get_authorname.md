---
UID: NF:qnetwork.IAMMediaContent.get_AuthorName
title: IAMMediaContent::get_AuthorName (qnetwork.h)
description: The get_AuthorName method retrieves the author name.helpviewer_keywords: ["IAMMediaContent interface [DirectShow]","get_AuthorName method","IAMMediaContent.get_AuthorName","IAMMediaContent::get_AuthorName","IAMMediaContentget_AuthorName","dshow.iammediacontent_get_authorname","get_AuthorName","get_AuthorName method [DirectShow]","get_AuthorName method [DirectShow]","IAMMediaContent interface","qnetwork/IAMMediaContent::get_AuthorName"]
old-location: dshow\iammediacontent_get_authorname.htm
tech.root: DirectShow
ms.assetid: 49ccb07c-1f20-47e9-a05b-f8f3b77acc99
ms.date: 12/05/2018
ms.keywords: IAMMediaContent interface [DirectShow],get_AuthorName method, IAMMediaContent.get_AuthorName, IAMMediaContent::get_AuthorName, IAMMediaContentget_AuthorName, dshow.iammediacontent_get_authorname, get_AuthorName, get_AuthorName method [DirectShow], get_AuthorName method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_AuthorName
f1_keywords:
- qnetwork/IAMMediaContent.get_AuthorName
dev_langs:
- c++
req.header: qnetwork.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Qnetwork.h
api_name:
- IAMMediaContent.get_AuthorName
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMediaContent::get_AuthorName


## -description



The <code>get_AuthorName</code> method retrieves the author name.




## -parameters




### -param pbstrAuthorName

Pointer to a variable that receives a <b>BSTR</b> with the information.


## -returns



Returns an <b>HRESULT</b> value. Possible values include those shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Item not found.

</td>
</tr>
</table>
 




## -remarks



If the method succeeds, the caller must free the returned <b>BSTR</b> by calling the <b>SysFreeString</b> function.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/qnetwork/nn-qnetwork-iammediacontent">IAMMediaContent Interface</a>
 

 

