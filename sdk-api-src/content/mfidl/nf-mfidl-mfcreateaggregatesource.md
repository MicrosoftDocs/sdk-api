---
UID: NF:mfidl.MFCreateAggregateSource
title: MFCreateAggregateSource function
author: windows-sdk-content
description: Creates a media source that aggregates a collection of media sources.
old-location: mf\mfcreateaggregatesource.htm
tech.root: medfound
ms.assetid: 7288bd4b-6a74-4528-854d-d82783630422
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: MFCreateAggregateSource, MFCreateAggregateSource function [Media Foundation], mf.mfcreateaggregatesource, mfidl/MFCreateAggregateSource
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateAggregateSource
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MFCreateAggregateSource function


## -description


Creates a media source that aggregates a collection of media sources. 


## -parameters




### -param pSourceCollection [in]

A pointer to the <a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a> interface of the collection object that contains a list of media sources. 


### -param ppAggSource [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> interface of the aggregated media source. The caller must release the interface.


## -returns



The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.



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
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>pSourceCollection</i> collection does not contain any elements.

</td>
</tr>
</table>
 




## -remarks



The aggregated media source is useful for combining  streams from separate media sources. For example, you can use it to  combine a video capture source and an audio capture source. 


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT CreateAggregatedSource(
    IMFMediaSource *pSource1,
    IMFMediaSource *pSource2,
    IMFMediaSource **ppAggSource
    )
{
    *ppAggSource = NULL;

    IMFCollection *pCollection = NULL;

    HRESULT hr = MFCreateCollection(&amp;pCollection);

    if (SUCCEEDED(hr))
    {
        hr = pCollection-&gt;AddElement(pSource1);
    }
    if (SUCCEEDED(hr))
    {
        hr = pCollection-&gt;AddElement(pSource2);
    }
    if (SUCCEEDED(hr))
    {
        hr = MFCreateAggregateSource(pCollection, ppAggSource);
    }
    SafeRelease(&amp;pCollection);
    return hr;    
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a>



<a href="https://msdn.microsoft.com/3018ffa7-e709-45b0-8b2b-7640d5633378">Media Foundation Functions</a>
 

 

