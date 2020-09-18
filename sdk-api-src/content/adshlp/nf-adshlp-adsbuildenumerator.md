---
UID: NF:adshlp.ADsBuildEnumerator
title: ADsBuildEnumerator function (adshlp.h)
description: The ADsBuildEnumerator function creates an enumerator object for the specified ADSI container object.
helpviewer_keywords: ["ADsBuildEnumerator","ADsBuildEnumerator function [ADSI]","_ds_adsbuildenumerator","adshlp/ADsBuildEnumerator","adsi.adsbuildenumerator"]
old-location: adsi\adsbuildenumerator.htm
tech.root: adsi
ms.assetid: e4fdec19-bccf-49ec-8a95-29e096c4c9c1
ms.date: 12/05/2018
ms.keywords: ADsBuildEnumerator, ADsBuildEnumerator function [ADSI], _ds_adsbuildenumerator, adshlp/ADsBuildEnumerator, adsi.adsbuildenumerator
req.header: adshlp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Activeds.lib
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ADsBuildEnumerator
 - adshlp/ADsBuildEnumerator
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsBuildEnumerator
---

# ADsBuildEnumerator function


## -description

The <b>ADsBuildEnumerator</b> function creates an enumerator object for the specified ADSI container object.

## -parameters

### -param pADsContainer [in]

Type: <b>IADsContainer*</b>

Pointer to the  <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interface for the object to enumerate.

### -param ppEnumVariant [out]

Type: <b>IEnumVARIANT**</b>

Pointer to an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface pointer that receives the enumerator object created for the specified container object.

## -returns

Type: <b>HRESULT</b>

This method supports the standard <b>HRESULT</b> return values, including <b>S_OK</b> for a successful operation. For more information about other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The <b>ADsBuildEnumerator</b> helper function wraps the calls used to retrieve the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> interface on the enumerator object.

<p class="proch"><b> To enumerate the available objects in a container</b>

<ol>
<li>Call the <b>ADsBuildEnumerator</b> function to create an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a> object that will enumerate the contents of the container.</li>
<li>Call the <a href="/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext">ADsEnumerateNext</a> function as many times as necessary to retrieve the items from the enumerator object.</li>
<li>Call the <a href="/windows/desktop/api/adshlp/nf-adshlp-adsfreeenumerator">ADSFreeEnumerator</a> function to release the enumerator object when it is no longer required.</li>
</ol>
If the server supports paged searches and the client has specified a page size that exceeds the maximum search results allowed by the server, the <b>ADsBuildEnumerator</b> function will forward errors and results from the server to the user.


#### Examples

The following code example shows how the <b>ADsBuildEnumerator</b>, <a href="/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext">ADsEnumerateNext</a>, and <a href="/windows/desktop/api/adshlp/nf-adshlp-adsfreeenumerator">ADSFreeEnumerator</a> functions can be used to enumerate the contents of a container.


```cpp
HRESULT PrintAllObjects(IADsContainer* pContainer)
{
    HRESULT hr;
     
    if(NULL == pContainer) 
    {
        return E_INVALIDARG;
    }
     
    IEnumVARIANT *pEnum = NULL;

    // Create an enumerator object in the container.
    hr = ADsBuildEnumerator(pContainer, &pEnum);
    if(SUCCEEDED(hr))
    {
        VARIANT var;
        ULONG ulFetched = 0L;

        // Get the next contained object.
        while(S_OK == (hr = ADsEnumerateNext(pEnum, 1, &var, &ulFetched)) && (ulFetched > 0))
        {
            IADs *pADs;

            // Print the object
            hr = V_DISPATCH(&var)->QueryInterface(IID_IADs, (void**)&pADs);
            if(SUCCEEDED(hr))
            {
                CComBSTR sbstr;
                IADsContainer *pChildContainer;

                hr = pADs->get_Name(&sbstr);
                if(SUCCEEDED(hr))
                {
                    wprintf(sbstr);
                    wprintf(L"\n");
                }

                hr = pADs->QueryInterface(IID_IADsContainer, (void**)&pChildContainer);
                if(SUCCEEDED(hr))
                {
                    // If the retrieved object is a container, recursively print its contents as well.
                    PrintAllObjects(pChildContainer);
                }
                
                pADs->Release();
            }
            
            // Release the VARIANT.
            VariantClear(&var);
        }
        
        ADsFreeEnumerator(pEnum);
    }

    return hr;
}

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-functions">ADSI Functions</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsenumeratenext">ADsEnumerateNext</a>



<a href="/windows/desktop/api/adshlp/nf-adshlp-adsfreeenumerator">ADsFreeEnumerator</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>