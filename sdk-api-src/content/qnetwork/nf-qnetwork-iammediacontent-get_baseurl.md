---
UID: NF:qnetwork.IAMMediaContent.get_BaseURL
title: IAMMediaContent::get_BaseURL (qnetwork.h)
author: windows-sdk-content
description: The get_BaseURL method gets a base URL for the related web content.
old-location: dshow\iammediacontent_get_baseurl.htm
tech.root: DirectShow
ms.assetid: 0fd88d09-79bf-45c6-93b4-1f57752ed1cd
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMMediaContent interface [DirectShow],get_BaseURL method, IAMMediaContent.get_BaseURL, IAMMediaContent::get_BaseURL, IAMMediaContentget_BaseURL, dshow.iammediacontent_get_baseurl, get_BaseURL, get_BaseURL method [DirectShow], get_BaseURL method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_BaseURL
ms.topic: method
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
 - IAMMediaContent.get_BaseURL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaContent::get_BaseURL


## -description



The <b>get_BaseURL</b> method gets a base URL for the related web content.




## -parameters




### -param pbstrBaseURL

Receives a <b>BSTR</b> with the information.
          


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd319638(v=VS.85).aspx">IAMMediaContent Interface</a>
 

 

