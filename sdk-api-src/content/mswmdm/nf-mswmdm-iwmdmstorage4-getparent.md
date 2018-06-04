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

# IWMDMStorage4::GetParent


## -description



The <b>GetParent</b> method retrieves the parent of the storage.




## -parameters




### -param ppStorage [out]

Pointer to the <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface of the parent storage. The caller must release this interface when finished with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The application can navigate up the storage hierarchy by calling <b>GetParent</b> recursively. After the root storage is reached, <b>GetParent</b> returns S_FALSE and sets <i>ppStorage</i> to <b>NULL</b>.


#### Examples

The following C++ function traverses up to the root parent of a storage.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT BubbleUp(IWMDMStorage *pIStorage)
{
    HRESULT hr = S_OK;
    CComPtr&lt;IWMDMStorage4&gt; pStorage4;

    hr = pIStorage-&gt;QueryInterface (__uuidof(IWMDMStorage4), reinterpret_cast&lt;void**&gt;(&amp;pStorage4));
    if (SUCCEEDED(hr))
    {
        while ((pStorage4 != NULL))
        {
            CComPtr&lt;IWMDMStorage&gt; pParent;
            hr = pStorage4-&gt;GetParent(&amp;pParent);
            if (FAILED(hr))
            {
                break;
            }

            //
            // Do something with pParent....
            //
            
            if (S_FALSE != hr)
            {
                hr = pParent-&gt;QueryInterface (__uuidof(IMDSPStorage4), reinterpret_cast&lt;void**&gt;(&amp;pStorage4));
                if (FAILED(hr))
                {
                    break;
                }
            }
        } // Loop up to next parent.
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>
 

 

