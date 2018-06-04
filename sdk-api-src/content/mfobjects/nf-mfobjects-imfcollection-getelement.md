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

# IMFCollection::GetElement


## -description



Retrieves an object in the collection.




## -parameters




### -param dwElementIndex [in]


            Zero-based index of the object to retrieve. Objects are indexed in the order in which they were added to the collection.
          


### -param ppUnkElement [out]


            Receives a pointer to the object's <b>IUnknown</b> interface. The caller must release the interface. The retrieved pointer value might be <b>NULL</b>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        This method does not remove the object from the collection. To remove an object, call <a href="https://msdn.microsoft.com/47f33235-6bb5-4103-82b4-87210b0e695c">IMFCollection::RemoveElement</a>.
      


#### Examples

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//  Gets an interface pointer from a collection (IMFCollection).
//
//  Q: Interface type

template &lt;class Q&gt;
HRESULT GetCollectionObject(IMFCollection *pCollection, 
    DWORD dwIndex, Q **ppObject)
{
    *ppObject = NULL;   // zero output

    IUnknown *pUnk = NULL;
    HRESULT hr = pCollection-&gt;GetElement(dwIndex, &amp;pUnk);
    if (SUCCEEDED(hr))
    {
        hr = pUnk-&gt;QueryInterface(IID_PPV_ARGS(ppObject));
        pUnk-&gt;Release();
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/fec6aa17-2770-4f53-b36d-b94236093d23">IMFCollection</a>
 

 

