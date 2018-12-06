---
UID: NF:qnetwork.IAMMediaContent.get_Description
title: IAMMediaContent::get_Description
author: windows-sdk-content
description: The get_Description method retrieves a description of the content.
old-location: dshow\iammediacontent_get_description.htm
tech.root: DirectShow
ms.assetid: fc0c14f3-2764-4897-8ddb-ed1146d98597
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAMMediaContent interface [DirectShow],get_Description method, IAMMediaContent.get_Description, IAMMediaContent::get_Description, IAMMediaContentget_Description, dshow.iammediacontent_get_description, get_Description, get_Description method [DirectShow], get_Description method [DirectShow],IAMMediaContent interface, qnetwork/IAMMediaContent::get_Description
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
 - IAMMediaContent.get_Description
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaContent::get_Description


## -description



The <code>get_Description</code> method retrieves a description of the content.




## -parameters




### -param pbstrDescription

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
 

 

