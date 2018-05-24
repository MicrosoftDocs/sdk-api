---
UID: NF:qnetwork.IAMMediaContent.get_LogoURL
title: IAMMediaContent::get_LogoURL
author: windows-driver-content
description: The get_LogoURL method retrieves a URL for the logo.
old-location: dshow\iammediacontent_get_logourl.htm
old-project: DirectShow
ms.assetid: 9a17c080-49a9-4b0b-8d94-054ad53b95b8
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IAMMediaContent interface [DirectShow],get_LogoURL method, IAMMediaContent.get_LogoURL, IAMMediaContent::get_LogoURL, IAMMediaContentget_LogoURL, dshow.iammediacontent_get_logourl, get_LogoURL, get_LogoURL method [DirectShow], get_LogoURL method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_LogoURL
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: AMExtendedSeekingCapabilities
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Qnetwork.h
api_name:
-	IAMMediaContent.get_LogoURL
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IAMMediaContent::get_LogoURL


## -description



The <code>get_LogoURL</code> method retrieves a URL for the logo.




## -parameters




### -param pbstrLogoURL

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
 

 

