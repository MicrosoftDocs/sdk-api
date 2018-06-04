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

# IMFMetadata::GetAllLanguages


## -description



          Gets a list of the languages in which metadata is available.


## -parameters




### -param ppvLanguages [out]


            A pointer to a <b>PROPVARIANT</b> that receives the list of languages. The list is returned as an array of null-terminated wide-character strings. Each string in the array is an RFC 1766-compliant language tag. 

The returned <b>PROPVARIANT</b> type is VT_VECTOR | VT_LPWSTR. The list might be empty, if no language tags are present. The caller must free the <b>PROPVARIANT</b> by calling <a href="https://msdn.microsoft.com/062b6065-a56f-4ecd-b232-3ba338a6d806">PropVariantClear</a>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks




        For more information about language tags, see RFC 1766, "Tags for the Identification of Languages".
      


        To set the current language, call <a href="https://msdn.microsoft.com/da615053-ddd5-448e-905c-b060cdaefa95">IMFMetadata::SetLanguage</a>.
      


#### Examples

The following example shows how to get the list of language tags and enumerate the list.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DisplayLanguageList(IMFMetadata *pMetadata)
{
    PROPVARIANT varLangs;

    HRESULT hr = pMetadata-&gt;GetAllLanguages(&amp;varLangs);
    if (SUCCEEDED(hr))
    {
        if (varLangs.vt == (VT_VECTOR | VT_LPWSTR))
        {
            for (ULONG i = 0; i &lt; varLangs.calpwstr.cElems; i++)
            {
                wprintf(L"%s\n", varLangs.calpwstr.pElems[i]);
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
        PropVariantClear(&amp;varLangs);
    }
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/411658ca-dc5e-445b-8d61-0c0429fcfbb1">IMFMetadata</a>



<a href="https://msdn.microsoft.com/dd7c4bc9-e2a6-49cd-8f29-865a44d5b5c9">Media Metadata</a>
 

 

