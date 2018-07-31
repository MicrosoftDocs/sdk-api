---
UID: NF:strmif.IBaseFilter.QueryFilterInfo
title: IBaseFilter::QueryFilterInfo
author: windows-sdk-content
description: The QueryFilterInfo method retrieves information about the filter.
old-location: dshow\ibasefilter_queryfilterinfo.htm
old-project: DirectShow
ms.assetid: 6cb9b6ef-05ae-4816-b337-dd90cab843fb
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IBaseFilter interface [DirectShow],QueryFilterInfo method, IBaseFilter.QueryFilterInfo, IBaseFilter::QueryFilterInfo, IBaseFilterQueryFilterInfo, QueryFilterInfo, QueryFilterInfo method [DirectShow], QueryFilterInfo method [DirectShow],IBaseFilter interface, dshow.ibasefilter_queryfilterinfo, strmif/IBaseFilter::QueryFilterInfo
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IBaseFilter.QueryFilterInfo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IBaseFilter::QueryFilterInfo


## -description



The <code>QueryFilterInfo</code> method retrieves information about the filter.




## -parameters




### -param pInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/43d1951e-448d-4139-879b-3fe021490d7d">FILTER_INFO</a> structure.


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
Success

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument

</td>
</tr>
</table>
 




## -remarks



This method fills the <b>FILTER_INFO</b> structure with the filter information. On return, if the <b>pGraph</b> member of the <b>FILTER_INFO</b> structure is non-<b>NULL</b>, the <a href="https://msdn.microsoft.com/73a92f44-03c6-47e3-98d1-a20100ed8fa1">IFilterGraph</a> interface has an outstanding reference count. Be sure to release the interface when you are done.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/d8c09dc7-dae8-4b51-8da8-69e64928a091">IBaseFilter Interface</a>
 

 

