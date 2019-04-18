---
UID: NF:adshlp.ADsBuildEnumerator
title: ADsBuildEnumerator function (adshlp.h)
author: windows-sdk-content
description: The ADsBuildEnumerator function creates an enumerator object for the specified ADSI container object.
old-location: adsi\adsbuildenumerator.htm
tech.root: adsi
ms.assetid: e4fdec19-bccf-49ec-8a95-29e096c4c9c1
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ADsBuildEnumerator, ADsBuildEnumerator function [ADSI], _ds_adsbuildenumerator, adshlp/ADsBuildEnumerator, adsi.adsbuildenumerator
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Activeds.dll
api_name:
 - ADsBuildEnumerator
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ADsBuildEnumerator function


## -description


The <b>ADsBuildEnumerator</b> function creates an enumerator object for the specified ADSI container object.


## -parameters




### -param pADsContainer [in]

Type: <b>IADsContainer*</b>

Pointer to the  <a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a> interface for the object to enumerate.


### -param ppEnumVariant [out]

Type: <b>IEnumVARIANT**</b>

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface pointer that receives the enumerator object created for the specified container object.


## -returns



Type: <b>HRESULT</b>

This method supports the standard <b>HRESULT</b> return values, including <b>S_OK</b> for a successful operation. For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The <b>ADsBuildEnumerator</b> helper function wraps the calls used to retrieve the <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> interface on the enumerator object.

<p class="proch"><img alt="" src="../common/wedge.gif"/><b> To enumerate the available objects in a container</b>

<ol>
<li>Call the <b>ADsBuildEnumerator</b> function to create an <a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a> object that will enumerate the contents of the container.</li>
<li>Call the <a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a> function as many times as necessary to retrieve the items from the enumerator object.</li>
<li>Call the <a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADSFreeEnumerator</a> function to release the enumerator object when it is no longer required.</li>
</ol>
If the server supports paged searches and the client has specified a page size that exceeds the maximum search results allowed by the server, the <b>ADsBuildEnumerator</b> function will forward errors and results from the server to the user.


#### Examples

The following code example shows how the <b>ADsBuildEnumerator</b>, <a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a>, and <a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADSFreeEnumerator</a> functions can be used to enumerate the contents of a container.


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




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/9bfc98a5-f4f0-4127-89c9-b8ed01bfde4e">ADsEnumerateNext</a>



<a href="https://msdn.microsoft.com/0ac13320-c0c2-45e3-b1c0-b4bf6c7e5315">ADsFreeEnumerator</a>



<a href="https://msdn.microsoft.com/6c1d6c7c-e003-47f9-adfa-4a753fb3e9b2">IADsContainer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221053(v=VS.85).aspx">IEnumVARIANT</a>
 

 

