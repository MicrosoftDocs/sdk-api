---
UID: NF:mfobjects.IMFCollection.GetElement
title: IMFCollection::GetElement
author: windows-sdk-content
description: Retrieves an object in the collection.
old-location: mf\imfcollection_getelement.htm
tech.root: medfound
ms.assetid: a45983a8-4061-40e1-a11a-67de0867e553
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetElement, GetElement method [Media Foundation], GetElement method [Media Foundation],IMFCollection interface, IMFCollection interface [Media Foundation],GetElement method, IMFCollection.GetElement, IMFCollection::GetElement, a45983a8-4061-40e1-a11a-67de0867e553, mf.imfcollection_getelement, mfobjects/IMFCollection::GetElement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFCollection.GetElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
 

 

