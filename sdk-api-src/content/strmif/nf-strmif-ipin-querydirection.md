---
UID: NF:strmif.IPin.QueryDirection
title: IPin::QueryDirection
author: windows-sdk-content
description: The QueryDirection method gets the direction of the pin (input or output).
old-location: dshow\ipin_querydirection.htm
tech.root: DirectShow
ms.assetid: cc36b5d6-bcca-403d-b840-ceabbf159f5d
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IPin interface [DirectShow],QueryDirection method, IPin.QueryDirection, IPin::QueryDirection, IPinQueryDirection, QueryDirection, QueryDirection method [DirectShow], QueryDirection method [DirectShow],IPin interface, dshow.ipin_querydirection, strmif/IPin::QueryDirection
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IPin.QueryDirection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPin::QueryDirection


## -description



The <b>QueryDirection</b> method gets the direction of the pin (input or output).




## -parameters




### -param pPinDir [out]

Receives a member of the <a href="https://msdn.microsoft.com/87f4e2e8-543f-46a3-b385-cc2e6af39770">PIN_DIRECTION</a> enumerated type.
          


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
 




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin Interface</a>
 

 

