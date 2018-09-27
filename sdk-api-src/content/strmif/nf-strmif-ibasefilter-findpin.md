---
UID: NF:strmif.IBaseFilter.FindPin
title: IBaseFilter::FindPin
author: windows-sdk-content
description: The FindPin method retrieves the pin with the specified identifier.
old-location: dshow\ibasefilter_findpin.htm
tech.root: DirectShow
ms.assetid: 0bdefaeb-f631-4b79-9965-c1c570e0ff80
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: FindPin, FindPin method [DirectShow], FindPin method [DirectShow],IBaseFilter interface, IBaseFilter interface [DirectShow],FindPin method, IBaseFilter.FindPin, IBaseFilter::FindPin, IBaseFilterFindPin, dshow.ibasefilter_findpin, strmif/IBaseFilter::FindPin
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
 - IBaseFilter.FindPin
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IBaseFilter::FindPin


## -description



The <code>FindPin</code> method retrieves the pin with the specified identifier.




## -parameters




### -param Id [in]

Pointer to a constant wide-character string that identifies the pin. Call the <a href="https://msdn.microsoft.com/d4fb2713-549d-4c0d-9768-386bcffd696f">IPin::QueryId</a> method to retrieve a pin's identifier.


### -param ppPin [out]

Address of a variable that receives a pointer to the pin's <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface. If the method fails, <i>*ppPin</i> is set to <b>NULL</b>.


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
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
Could not find a pin with this identifier.

</td>
</tr>
</table>
 




## -remarks



This method supports graph persistence. Use the <a href="https://msdn.microsoft.com/d4fb2713-549d-4c0d-9768-386bcffd696f">IPin::QueryId</a> method to save a pin's state, and use this method to restore the state. The pin's identifier string is defined by the filter implementation. The identifier must be unique within the filter.

If the method succeeds, the <b>IPin</b> interface that it returns has an outstanding reference count. Be sure to release the interface when you are done.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter Interface</a>
 

 

