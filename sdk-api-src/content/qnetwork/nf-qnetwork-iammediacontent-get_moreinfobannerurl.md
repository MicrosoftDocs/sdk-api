---
UID: NF:qnetwork.IAMMediaContent.get_MoreInfoBannerURL
title: IAMMediaContent::get_MoreInfoBannerURL
author: windows-sdk-content
description: The get_MoreInfoBannerURL method retrieves a URL for a related-information banner.
old-location: dshow\iammediacontent_get_moreinfobannerurl.htm
old-project: DirectShow
ms.assetid: cc820849-cab2-4770-bdb2-6c4b32f3cc56
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IAMMediaContent interface [DirectShow],get_MoreInfoBannerURL method, IAMMediaContent.get_MoreInfoBannerURL, IAMMediaContent::get_MoreInfoBannerURL, IAMMediaContentget_MoreInfoBannerURL, dshow.iammediacontent_get_moreinfobannerurl, get_MoreInfoBannerURL, get_MoreInfoBannerURL method [DirectShow], get_MoreInfoBannerURL method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_MoreInfoBannerURL
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AMExtendedSeekingCapabilities
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Qnetwork.h
api_name:
 - IAMMediaContent.get_MoreInfoBannerURL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IAMMediaContent::get_MoreInfoBannerURL


## -description



The <code>get_MoreInfoBannerURL</code> method retrieves a URL for a related-information banner.




## -parameters




### -param pbstrMoreInfoBannerURL

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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/bd9cc96d-9664-41f3-9d4f-e5bdb1cb8d09">IAMMediaContent Interface</a>
 

 

