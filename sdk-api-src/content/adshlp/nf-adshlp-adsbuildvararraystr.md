---
UID: NF:adshlp.ADsBuildVarArrayStr
title: ADsBuildVarArrayStr function (adshlp.h)
author: windows-sdk-content
description: The ADsBuildVarArrayStr function builds a variant array from an array of Unicode strings.
old-location: adsi\adsbuildvararraystr.htm
tech.root: adsi
ms.assetid: 7258a840-691a-4d9b-ab33-bcdf30fd1331
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ADsBuildVarArrayStr, ADsBuildVarArrayStr function [ADSI], _ds_adsbuildvararraystr, adshlp/ADsBuildVarArrayStr, adsi.adsbuildvararraystr
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
 - ADsBuildVarArrayStr
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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


```cpp
HRESULT EnumObject(LPWSTR pszADsPath,
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
                     (void**)&pADsContainer);
    if (FAILED(hr)) goto cleanup;
 
    // Create a string array of class names as search filters.
    VariantInit(&varFilter);
    hr = ADsBuildVarArrayStr(lppClsNames, dwClsNames, &varFilter);
    if (FAILED(hr)) goto cleanup;
 
    // Apply filters to objects in the container.
    hr = pADsContainer->put_Filter(varFilter);
    if(FAILED(hr)) goto cleanup;
 
    // Create an enumerator.
    hr = ADsBuildEnumerator(pADsContainer, &pEnumVar);
    if(FAILED(hr)) goto cleanup;
 
    // Enumerate the objects and print the names.
    while(fContinue) {
        IADs* pObject;
        hr = ADsEnumerateNext(pEnumVar, MAX_ADS_ENUM,
                            varArray, &ulFetched);
        if(hr == S_FALSE) fContinue = FALSE;
        dwEEnumCount++;
 
        for (i=0; i<ulFetched; i++) {
            IDispatch *pDispatch = NULL;
            pDispatch = varArray[I].pDispVal;
            hr = pDispatch->QueryInterface(IID_IADs,
                                        (void**) &pObject);
            if (FAILED(hr)) goto cleanup;
 
            hr = pObject->get_Name(&bstrName);
            if(FAILED(hr)) goto cleanup;
            printf(" Object name: %S\n",bstrName);
 
            // Release the ADSI object.
            SysFreeString(bstrname);
            pObject->Release();
            pDispatch->Release();
        }
        memset(varArray, 0, sizeof(VARIANT)*MAX_ADS_ENUM);
        dwObjects += ulFetched;
    }
    hr = S_OK;
 
cleanup:
    if(bstrName) SysFreeString(bstrName);
    if(pEnumvar) ADsFreeEnumerator(pEnumVar);
    if(pADsContainer) pADsContainer->Release();
 
    return (hr);
}
```





## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/4f0e90e2-afcc-4cf7-a731-9b38a83ca229">ADSI Functions</a>



<a href="https://msdn.microsoft.com/61b8a3c1-b8ea-4909-b2a6-f1ce342f396d">ADsBuildVarArrayInt</a>
 

 

