---
UID: NF:mfidl.IMFMetadata.GetAllLanguages
title: IMFMetadata::GetAllLanguages (mfidl.h)
description: Gets a list of the languages in which metadata is available.
helpviewer_keywords: ["69296ec5-5811-4f0f-ae9c-cabca3e66158","GetAllLanguages","GetAllLanguages method [Media Foundation]","GetAllLanguages method [Media Foundation]","IMFMetadata interface","IMFMetadata interface [Media Foundation]","GetAllLanguages method","IMFMetadata.GetAllLanguages","IMFMetadata::GetAllLanguages","mf.imfmetadata_getalllanguages","mfidl/IMFMetadata::GetAllLanguages"]
old-location: mf\imfmetadata_getalllanguages.htm
tech.root: mf
ms.assetid: 69296ec5-5811-4f0f-ae9c-cabca3e66158
ms.date: 12/05/2018
ms.keywords: 69296ec5-5811-4f0f-ae9c-cabca3e66158, GetAllLanguages, GetAllLanguages method [Media Foundation], GetAllLanguages method [Media Foundation],IMFMetadata interface, IMFMetadata interface [Media Foundation],GetAllLanguages method, IMFMetadata.GetAllLanguages, IMFMetadata::GetAllLanguages, mf.imfmetadata_getalllanguages, mfidl/IMFMetadata::GetAllLanguages
req.header: mfidl.h
req.include-header: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFMetadata::GetAllLanguages
 - mfidl/IMFMetadata::GetAllLanguages
dev_langs:
 - c++
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
---

# IMFMetadata::GetAllLanguages


## -description

Gets a list of the languages in which metadata is available.

## -parameters

### -param ppvLanguages [out]

A pointer to a <b>PROPVARIANT</b> that receives the list of languages. The list is returned as an array of null-terminated wide-character strings. Each string in the array is an RFC 1766-compliant language tag. 

The returned <b>PROPVARIANT</b> type is VT_VECTOR | VT_LPWSTR. The list might be empty, if no language tags are present. The caller must free the <b>PROPVARIANT</b> by calling <a href="/windows/desktop/api/propidl/nf-propidl-propvariantclear">PropVariantClear</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For more information about language tags, see RFC 1766, "Tags for the Identification of Languages".
      

To set the current language, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmetadata-setlanguage">IMFMetadata::SetLanguage</a>.
      


#### Examples

The following example shows how to get the list of language tags and enumerate the list.


```cpp
HRESULT DisplayLanguageList(IMFMetadata *pMetadata)
{
    PROPVARIANT varLangs;

    HRESULT hr = pMetadata->GetAllLanguages(&varLangs);
    if (SUCCEEDED(hr))
    {
        if (varLangs.vt == (VT_VECTOR | VT_LPWSTR))
        {
            for (ULONG i = 0; i < varLangs.calpwstr.cElems; i++)
            {
                wprintf(L"%s\n", varLangs.calpwstr.pElems[i]);
            }
        }
        else
        {
            hr = E_UNEXPECTED;
        }
        PropVariantClear(&varLangs);
    }
    return hr;
}

```

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfmetadata">IMFMetadata</a>



<a href="/windows/desktop/medfound/media-metadata">Media Metadata</a>