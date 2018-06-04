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

# ADsBuildVarArrayStr function


## -description


The <b>ADsBuildVarArrayStr</b> function builds a variant array from an array of Unicode strings.


## -parameters




### -param lppPathNames [in]

Type: <b>LPWSTR*</b>

Array of null-terminated Unicode strings.


### -param dwPathNames [in]

Type: <b>DWORD</b>

Number of Unicode entries in the given array.


### -param pVar [out]

Type: <b>VARIANT*</b>

Pointer to the resulting variant array.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values, as well as the following.

For more information about other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



To support Automation, use the <b>ADsBuildVarArrayStr</b> function to convert Unicode strings to a variant array of strings.


#### Examples

The following code example shows how to use the <b>ADsBuildVarArrayStr</b> function to convert object class names from Unicode strings to a variant array of strings.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT EnumObject(LPWSTR pszADsPath,
                   LPWSTR * lppClsNames,
                   DWORD dwClsNames)
{
    ULONG ulFetched = 0L;
    IEnumVARIANT * pEnumVar = NULL;
    VARIANT varFilter, varArray[MAX_ADS_ENUM];
    HRESULT hr;
    IADsContainer * pADsContainer = NULL;
    DWORD dwObjects = 0, dwEnumCount=0, i=0;
    BSTR bstrName;
    BOOL fContinue=TRUE;
 
    hr = ADsGetObject(pszADsPath,
                     IID_IADsContainer,
                     (void**)&amp;pADsContainer);
    if (FAILED(hr)) goto cleanup;
 
    // Create a string array of class names as search filters.
    VariantInit(&amp;varFilter);
    hr = ADsBuildVarArrayStr(lppClsNames, dwClsNames, &amp;varFilter);
    if (FAILED(hr)) goto cleanup;
 
    // Apply filters to objects in the container.
    hr = pADsContainer-&gt;put_Filter(varFilter);
    if(FAILED(hr)) goto cleanup;
 
    // Create an enumerator.
    hr = ADsBuildEnumerator(pADsContainer, &amp;pEnumVar);
    if(FAILED(hr)) goto cleanup;
 
    // Enumerate the objects and print the names.
    while(fContinue) {
        IADs* pObject;
        hr = ADsEnumerateNext(pEnumVar, MAX_ADS_ENUM,
                            varArray, &amp;ulFetched);
        if(hr == S_FALSE) fContinue = FALSE;
        dwEEnumCount++;
 
        for (i=0; i&lt;ulFetched; i++) {
            IDispatch *pDispatch = NULL;
            pDispatch = varArray[I].pDispVal;
            hr = pDispatch-&gt;QueryInterface(IID_IADs,
                                        (void**) &amp;pObject);
            if (FAILED(hr)) goto cleanup;
 
            hr = pObject-&gt;get_Name(&amp;bstrName);
            if(FAILED(hr)) goto cleanup;
            printf(" Object name: %S\n",bstrName);
 
            // Release the ADSI object.
            SysFreeString(bstrname);
            pObject-&gt;Release();
            pDispatch-&gt;Release();
        }
        memset(varArray, 0, sizeof(VARIANT)*MAX_ADS_ENUM);
        dwObjects += ulFetched;
    }
    hr = S_OK;
 
cleanup:
    if(bstrName) SysFreeString(bstrName);
    if(pEnumvar) ADsFreeEnumerator(pEnumVar);
    if(pADsContainer) pADsContainer-&gt;Release();
 
    return (hr);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/61b8a3c1-b8ea-4909-b2a6-f1ce342f396d">ADsBuildVarArrayInt</a>
 

 

