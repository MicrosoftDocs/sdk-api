---
UID: NF:d2d1_1.ID2D1CommandList.Close
title: ID2D1CommandList::Close (d2d1_1.h)
description: Instructs the command list to stop accepting commands so that you can use it as an input to an effect or in a call to ID2D1DeviceContext::DrawImage.
helpviewer_keywords: ["Close","Close method [Direct2D]","Close method [Direct2D]","ID2D1CommandList interface","ID2D1CommandList interface [Direct2D]","Close method","ID2D1CommandList.Close","ID2D1CommandList::Close","d2d1_1/ID2D1CommandList::Close","direct2d.id2d1commandlist_close"]
old-location: direct2d\id2d1commandlist_close.htm
tech.root: Direct2D
ms.assetid: 161A8E33-25C7-4007-8397-D86EBA777D4D
ms.date: 12/05/2018
ms.keywords: Close, Close method [Direct2D], Close method [Direct2D],ID2D1CommandList interface, ID2D1CommandList interface [Direct2D],Close method, ID2D1CommandList.Close, ID2D1CommandList::Close, d2d1_1/ID2D1CommandList::Close, direct2d.id2d1commandlist_close
req.header: d2d1_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1CommandList::Close
 - d2d1_1/ID2D1CommandList::Close
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1CommandList.Close
---

# ID2D1CommandList::Close


## -description

Instructs the command list to stop accepting commands so that you can use it as an input to an effect or in a call to <a href="/windows/desktop/api/d2d1_1/nf-d2d1_1-id2d1commandsink-drawimage">ID2D1DeviceContext::DrawImage</a>.  You should call the method after it has been attached to an <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1devicecontext">ID2D1DeviceContext</a>  and written to but before the command list is used.



## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>D2DERR_WRONG_STATE </td>
<td>Close has already been called on the command list.</td>
</tr>
</table>
 


<div class="alert"><b>Note</b>  If the device context associated with the command list has an error, the command list returns the same error.</div>
<div> </div>

## -remarks

This method returns D2DERR_WRONG_STATE if it has already been called on the command list. If an error occurred on the device context during population, the method returns that error. Otherwise, the method returns S_OK. 

If the <b>Close</b> method returns an error, any future use of the command list results in the same error.

## -see-also

<a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1commandlist">ID2D1CommandList</a>
