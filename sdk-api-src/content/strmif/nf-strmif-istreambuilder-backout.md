---
UID: NF:strmif.IStreamBuilder.Backout
title: IStreamBuilder::Backout
author: windows-sdk-content
description: The Backout method undoes steps taken in the IStreamBuilder::Render method. This includes disconnecting and removing any filters that were added inside Render.
old-location: dshow\istreambuilder_backout.htm
tech.root: DirectShow
ms.assetid: b8f895a7-7f71-4c0d-af9d-e2b0ed433172
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: Backout, Backout method [DirectShow], Backout method [DirectShow],IStreamBuilder interface, IStreamBuilder interface [DirectShow],Backout method, IStreamBuilder.Backout, IStreamBuilder::Backout, IStreamBuilderBackout, dshow.istreambuilder_backout, strmif/IStreamBuilder::Backout
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
 - IStreamBuilder.Backout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


```cpp

STDMETHODIMP CMyOutputPin::BackOut(IPin *pPin, IGraphBuilder *pGraph)
{
    CheckPointer(pPin, E_POINTER);
    CheckPointer(pGraph, E_POINTER);

    HRESULT hr = S_OK;
    if (m_Connected != NULL) // Pointer to the pin we're connected to.
    {
        // Find the filter that owns the pin connected to us.
        FILTER_INFO fi;
        hr = m_Connected->QueryFilterInfo(&fi);
        if (SUCCEEDED(hr)) 
        {
            if (fi.pFilter != NULL) 
            {
                //  Disconnect the pins.
                pGraph->Disconnect(m_Connected);
                pGraph->Disconnect(pPin);
                // Remove the filter from the graph.
                pGraph->RemoveFilter(fi.pFilter);
                fi.pFilter->Release();
            } 
            else 
            {
                hr = E_UNEXPECTED;
            }
        }
    }
    return hr;
}

```





## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/233821e9-9916-4047-a554-4ff43769819f">IStreamBuilder Interface</a>
 

 

