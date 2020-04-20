---
UID: NF:strmif.IStreamBuilder.Backout
title: IStreamBuilder::Backout (strmif.h)
description: The Backout method undoes steps taken in the IStreamBuilder::Render method. This includes disconnecting and removing any filters that were added inside Render.helpviewer_keywords: ["Backout","Backout method [DirectShow]","Backout method [DirectShow]","IStreamBuilder interface","IStreamBuilder interface [DirectShow]","Backout method","IStreamBuilder.Backout","IStreamBuilder::Backout","IStreamBuilderBackout","dshow.istreambuilder_backout","strmif/IStreamBuilder::Backout"]
old-location: dshow\istreambuilder_backout.htm
tech.root: DirectShow
ms.assetid: b8f895a7-7f71-4c0d-af9d-e2b0ed433172
ms.date: 12/05/2018
ms.keywords: Backout, Backout method [DirectShow], Backout method [DirectShow],IStreamBuilder interface, IStreamBuilder interface [DirectShow],Backout method, IStreamBuilder.Backout, IStreamBuilder::Backout, IStreamBuilderBackout, dshow.istreambuilder_backout, strmif/IStreamBuilder::Backout
f1_keywords:
- strmif/IStreamBuilder.Backout
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
- IStreamBuilder.Backout
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStreamBuilder::Backout


## -description



The <code>Backout</code> method undoes steps taken in the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-istreambuilder-render">IStreamBuilder::Render</a> method. This includes disconnecting and removing any filters that were added inside <b>Render</b>.




## -parameters




### -param ppinOut [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ipin">IPin</a> interface of this pin.


### -param pGraph [in]

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-igraphbuilder">IGraphBuilder</a> interface of the Filter Graph Manager.


## -returns



Returns an <b>HRESULT</b> value. A return code of S_OK indicates to the graph builder that the disconnect was successful.




## -remarks



The following example shows how a filter would reverse the steps that are shown in the code example for the <b>IStreamBuilder::Render</b> method:

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
STDMETHODIMP CMyOutputPin::BackOut(IPin *pPin, IGraphBuilder *pGraph)
{
    CheckPointer(pPin, E_POINTER);
    CheckPointer(pGraph, E_POINTER);

    HRESULT hr = S_OK;
    if (m_Connected != NULL) // Pointer to the pin we're connected to.
    {
        // Find the filter that owns the pin connected to us.
        FILTER_INFO fi;
        hr = m_Connected-&gt;QueryFilterInfo(&amp;fi);
        if (SUCCEEDED(hr)) 
        {
            if (fi.pFilter != NULL) 
            {
                //  Disconnect the pins.
                pGraph-&gt;Disconnect(m_Connected);
                pGraph-&gt;Disconnect(pPin);
                // Remove the filter from the graph.
                pGraph-&gt;RemoveFilter(fi.pFilter);
                fi.pFilter-&gt;Release();
            } 
            else 
            {
                hr = E_UNEXPECTED;
            }
        }
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-istreambuilder">IStreamBuilder Interface</a>
 

 

