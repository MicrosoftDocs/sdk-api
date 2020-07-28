---
UID: NF:qnetwork.IAMMediaContent.get_Rating
title: IAMMediaContent::get_Rating (qnetwork.h)
description: The get_Rating method retrieves the rating.
helpviewer_keywords: ["IAMMediaContent interface [DirectShow]","get_Rating method","IAMMediaContent.get_Rating","IAMMediaContent::get_Rating","IAMMediaContentget_Rating","dshow.iammediacontent_get_rating","get_Rating","get_Rating method [DirectShow]","get_Rating method [DirectShow]","IAMMediaContent interface","qnetwork/IAMMediaContent::get_Rating"]
old-location: dshow\iammediacontent_get_rating.htm
tech.root: dshow
ms.assetid: 2eeb1356-23f5-48dc-be71-062f1501d163
ms.date: 12/05/2018
ms.keywords: IAMMediaContent interface [DirectShow],get_Rating method, IAMMediaContent.get_Rating, IAMMediaContent::get_Rating, IAMMediaContentget_Rating, dshow.iammediacontent_get_rating, get_Rating, get_Rating method [DirectShow], get_Rating method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_Rating
f1_keywords:
- qnetwork/IAMMediaContent.get_Rating
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
- IAMMediaContent.get_Rating
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAMMediaContent::get_Rating


## -description



The <code>get_Rating</code> method retrieves the rating.




## -parameters




### -param pbstrRating

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
 

 

