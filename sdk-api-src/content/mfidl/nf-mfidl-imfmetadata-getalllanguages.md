---
UID: NF:mfidl.IMFMetadata.GetAllLanguages
title: IMFMetadata::GetAllLanguages
author: windows-sdk-content
description: Gets a list of the languages in which metadata is available.
old-location: mf\imfmetadata_getalllanguages.htm
old-project: medfound
ms.assetid: 69296ec5-5811-4f0f-ae9c-cabca3e66158
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: 69296ec5-5811-4f0f-ae9c-cabca3e66158, GetAllLanguages, GetAllLanguages method [Media Foundation], GetAllLanguages method [Media Foundation],IMFMetadata interface, IMFMetadata interface [Media Foundation],GetAllLanguages method, IMFMetadata.GetAllLanguages, IMFMetadata::GetAllLanguages, mf.imfmetadata_getalllanguages, mfidl/IMFMetadata::GetAllLanguages
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: MFSensorDeviceMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFMetadata.GetAllLanguages
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
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
 

 

