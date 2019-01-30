---
UID: NF:strmif.IPin.QueryPinInfo
title: IPin::QueryPinInfo
author: windows-sdk-content
description: The QueryPinInfo method retrieves information about the pin.
old-location: dshow\ipin_querypininfo.htm
tech.root: DirectShow
ms.assetid: 1a7c85ce-46f1-4928-9e2a-3a4bd96dc771
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPin interface [DirectShow],QueryPinInfo method, IPin.QueryPinInfo, IPin::QueryPinInfo, IPinQueryPinInfo, QueryPinInfo, QueryPinInfo method [DirectShow], QueryPinInfo method [DirectShow],IPin interface, dshow.ipin_querypininfo, strmif/IPin::QueryPinInfo
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IPin.QueryPinInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPin::QueryPinInfo


## -description



The <code>QueryPinInfo</code> method retrieves information about the pin.




## -parameters




### -param pInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/67a837f3-8b81-4651-a0fa-fed7b61e71c2">PIN_INFO</a> structure that receives the pin information.


## -returns



Returns an <b>HRESULT</b> value. Possible values include the following.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
</table>
 




## -remarks



When the method returns, if the <b>pFilter</b> member of the PIN_INFO structure is non-<b>NULL</b>, it has an outstanding reference count. Be sure to release the interface when you are done.




## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

