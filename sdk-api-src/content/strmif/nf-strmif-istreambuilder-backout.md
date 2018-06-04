---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IStreamBuilder::Backout


## -description



The <code>Backout</code> method undoes steps taken in the <a href="https://msdn.microsoft.com/7bba9d1a-03a8-4572-a08c-2e12071df73b">IStreamBuilder::Render</a> method. This includes disconnecting and removing any filters that were added inside <b>Render</b>.




## -parameters




### -param ppinOut [in]

Pointer to the <a href="https://msdn.microsoft.com/ad0ead4e-9f8e-4935-b220-306d665e50f4">IPin</a> interface of this pin.


### -param pGraph [in]

Pointer to the <a href="https://msdn.microsoft.com/54ed8ac8-4821-4c0c-9fb9-789c70dbca37">IGraphBuilder</a> interface of the Filter Graph Manager.


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




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/233821e9-9916-4047-a554-4ff43769819f">IStreamBuilder Interface</a>
 

 

