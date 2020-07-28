---
UID: NF:strmif.IEnumFilters.Next
title: IEnumFilters::Next (strmif.h)
description: The Next method retrieves the specified number of filters in the enumeration sequence.
helpviewer_keywords: ["IEnumFilters interface [DirectShow]","Next method","IEnumFilters.Next","IEnumFilters::Next","IEnumFiltersNext","Next","Next method [DirectShow]","Next method [DirectShow]","IEnumFilters interface","dshow.ienumfilters_next","strmif/IEnumFilters::Next"]
old-location: dshow\ienumfilters_next.htm
tech.root: dshow
ms.assetid: 0e376a01-d353-434c-864a-8001c8022679
ms.date: 12/05/2018
ms.keywords: IEnumFilters interface [DirectShow],Next method, IEnumFilters.Next, IEnumFilters::Next, IEnumFiltersNext, Next, Next method [DirectShow], Next method [DirectShow],IEnumFilters interface, dshow.ienumfilters_next, strmif/IEnumFilters::Next
f1_keywords:
- strmif/IEnumFilters.Next
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
- IEnumFilters.Next
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IEnumFilters::Next


## -description



The <code>Next</code> method retrieves the specified number of filters in the enumeration sequence.




## -parameters




### -param cFilters [in]

Number of filters to retrieve.


### -param ppFilter [out]

Array of size <i>cFilters</i> that is filled with <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ibasefilter">IBaseFilter</a> interface pointers. The caller must release the interfaces.


### -param pcFetched [out]

Receives the number of filters retrieved. Can be <b>NULL</b> if <i>cFilters</i> is 1.


## -returns



<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>S_FALSE</td>
<td>Did not retrieve as many filters as requested.</td>
</tr>
<tr>
<td>S_OK</td>
<td>Success.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>Invalid argument.</td>
</tr>
<tr>
<td>E_POINTER</td>
<td><b>NULL</b> pointer argument.</td>
</tr>
<tr>
<td>VFW_E_ENUM_OUT_OF_SYNC</td>
<td>The graph has changed and is now inconsistent with the enumerator.</td>
</tr>
</table>
 




## -remarks



If the method succeeds, the <b>IBaseFilter</b> pointers all have outstanding reference counts. Be sure to release them when you are done.

If the filter graph changes (for example, the application removes a filter), the enumerator is no longer be consistent with the graph, and the method returns VFW_E_ENUM_OUT_OF_SYNC. Discard any data obtained from previous calls to the enumerator, because it might be invalid. Update the enumerator by calling the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ienumfilters-reset">IEnumFilters::Reset</a> method. You can then call the <code>Next</code> method safely.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ienumfilters">IEnumFilters Interface</a>
 

 

