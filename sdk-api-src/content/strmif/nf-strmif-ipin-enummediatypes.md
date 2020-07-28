---
UID: NF:strmif.IPin.EnumMediaTypes
title: IPin::EnumMediaTypes (strmif.h)
description: The EnumMediaTypes method enumerates the pin's preferred media types.
helpviewer_keywords: ["EnumMediaTypes","EnumMediaTypes method [DirectShow]","EnumMediaTypes method [DirectShow]","IPin interface","IPin interface [DirectShow]","EnumMediaTypes method","IPin.EnumMediaTypes","IPin::EnumMediaTypes","IPinEnumMediaTypes","dshow.ipin_enummediatypes","strmif/IPin::EnumMediaTypes"]
old-location: dshow\ipin_enummediatypes.htm
tech.root: dshow
ms.assetid: 288be4db-5236-40e5-bd92-d95b1bfb86fa
ms.date: 12/05/2018
ms.keywords: EnumMediaTypes, EnumMediaTypes method [DirectShow], EnumMediaTypes method [DirectShow],IPin interface, IPin interface [DirectShow],EnumMediaTypes method, IPin.EnumMediaTypes, IPin::EnumMediaTypes, IPinEnumMediaTypes, dshow.ipin_enummediatypes, strmif/IPin::EnumMediaTypes
f1_keywords:
- strmif/IPin.EnumMediaTypes
dev_langs:
- c++
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
- IPin.EnumMediaTypes
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPin::EnumMediaTypes


## -description



The <b>EnumMediaTypes</b> method enumerates the pin's preferred media types.




## -parameters




### -param ppEnum [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ienummediatypes">IEnumMediaTypes</a> interface. The caller must release the interface.
          


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
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The pin is not connected. Some pins do not enumerate media types unless the pin is connected to another filter.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ienummediatypes">IEnumMediaTypes</a> interface works like a standard COM enumerator. For more information, see <a href="https://docs.microsoft.com/windows/desktop/DirectShow/enumerating-objects-in-a-filter-graph">Enumerating Objects in a Filter Graph</a>. If the method succeeds, the <b>IEnumMediaTypes</b> interface has an outstanding reference count. Be sure to release it when you are done.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/data-flow-in-the-filter-graph">Data Flow in the Filter Graph</a>



<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin Interface</a>
 

 

