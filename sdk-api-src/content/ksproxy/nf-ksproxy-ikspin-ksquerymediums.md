---
UID: NF:ksproxy.IKsPin.KsQueryMediums
title: IKsPin::KsQueryMediums method
author: windows-driver-content
description: The KsQueryMediums method retrieves the mediums supported by a pin.
old-location: dshow\ikspin_ksquerymediums.htm
old-project: DirectShow
ms.assetid: 554bf968-6054-4f9d-95db-facf0444641f
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IKsPin, IKsPin interface [DirectShow], KsQueryMediums method, IKsPin::KsQueryMediums, IKsPinKsQueryMediums, KsQueryMediums method [DirectShow], KsQueryMediums method [DirectShow], IKsPin interface, KsQueryMediums,IKsPin.KsQueryMediums, dshow.ikspin_ksquerymediums, ksproxy/IKsPin::KsQueryMediums
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ksproxy.h
req.include-header: 
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
req.typenames: WAVEFORMATEXTENSIBLE, *PWAVEFORMATEXTENSIBLE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IKsPin.KsQueryMediums
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IKsPin::KsQueryMediums method


## -description



The <code>KsQueryMediums</code> method retrieves the mediums supported by a pin.




## -parameters




### -param MediumList






#### - ppmi [out]

Address of a pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff563441">KSMULTIPLE_ITEM</a> structure.


## -returns



If the method succeeds, it returns S_OK. If it fails, it returns an <b>HRESULT</b> error code.




## -remarks



This method returns a task-allocated <a href="https://msdn.microsoft.com/library/windows/hardware/ff563441">KSMULTIPLE_ITEM</a> structure, which is followed by zero or more <a href="https://msdn.microsoft.com/ed5614fe-bfeb-4ddf-a626-b14080f45b33">REGPINMEDIUM</a> structures. The <b>Count</b> member of the <b>KSMULTIPLE_ITEM</b> structure specifies the number of <b>REGPINMEDIUM</b> structures. Each <b>REGPINMEDIUM</b> structure defines a medium supported by the pin.

The caller must free the returned structures, using the <b>CoTaskMemFree</b> function.

You must include Ks.h before Ksproxy.h.


#### Examples

The following helper function attempts to match a pin against a specified medium.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT FindMatchingMedium(
    IPin *pPin, 
    REGPINMEDIUM *pMedium, 
    bool *pfMatch)
{
    IKsPin* pKsPin = NULL;
    KSMULTIPLE_ITEM *pmi;

    *pfMatch = false;
    HRESULT hr = pPin-&gt;QueryInterface(IID_IKsPin, (void **)&amp;pKsPin);
    if (FAILED(hr)) 
        return hr;  // Pin does not support IKsPin.

    hr = pKsPin-&gt;KsQueryMediums(&amp;pmi);
    pKsPin-&gt;Release();
    if (FAILED(hr))
        return hr;  // Pin does not support mediums.

    if (pmi-&gt;Count) 
    {
        // Use pointer arithmetic to reference the first medium structure.
        REGPINMEDIUM *pTemp = (REGPINMEDIUM*)(pmi + 1);
        for (ULONG i = 0; i &lt; pmi-&gt;Count; i++, pTemp++) 
        {
            if (pMedium-&gt;clsMedium == pTemp-&gt;clsMedium) 
            {
                *pfMatch = true;
                break;
            }
        }
    }        
    CoTaskMemFree(pmi);
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/14d9bef2-e8f0-49d5-bd89-69a95814cf8c">IKsPin Interface</a>



<a href="https://msdn.microsoft.com/864fc5ad-5aeb-4dc7-bdd2-2ad2bfb57741">WDM Class Driver Filters</a>
 

 

