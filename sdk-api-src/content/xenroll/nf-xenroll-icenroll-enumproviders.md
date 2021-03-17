---
UID: NF:xenroll.ICEnroll.enumProviders
title: ICEnroll::enumProviders (xenroll.h)
description: Retrieves the names of the available cryptographic service providers (CSPs) specified by the ProviderType property. This method was first defined in the ICEnroll interface.
helpviewer_keywords: ["CEnroll object [Security]","enumProviders method","ICEnroll interface [Security]","enumProviders method","ICEnroll.enumProviders","ICEnroll2 interface [Security]","enumProviders method","ICEnroll2::enumProviders","ICEnroll3 interface [Security]","enumProviders method","ICEnroll3::enumProviders","ICEnroll4 interface [Security]","enumProviders method","ICEnroll4::enumProviders","ICEnroll::enumProviders","enumProviders","enumProviders method [Security]","enumProviders method [Security]","CEnroll object","enumProviders method [Security]","ICEnroll interface","enumProviders method [Security]","ICEnroll2 interface","enumProviders method [Security]","ICEnroll3 interface","enumProviders method [Security]","ICEnroll4 interface","security.icenroll4_enumproviders","xenroll/ICEnroll2::enumProviders","xenroll/ICEnroll3::enumProviders","xenroll/ICEnroll4::enumProviders","xenroll/ICEnroll::enumProviders"]
old-location: security\icenroll4_enumproviders.htm
tech.root: security
ms.assetid: 05188aee-2b03-46bc-89f4-506a019496a4
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],enumProviders method, ICEnroll interface [Security],enumProviders method, ICEnroll.enumProviders, ICEnroll2 interface [Security],enumProviders method, ICEnroll2::enumProviders, ICEnroll3 interface [Security],enumProviders method, ICEnroll3::enumProviders, ICEnroll4 interface [Security],enumProviders method, ICEnroll4::enumProviders, ICEnroll::enumProviders, enumProviders, enumProviders method [Security], enumProviders method [Security],CEnroll object, enumProviders method [Security],ICEnroll interface, enumProviders method [Security],ICEnroll2 interface, enumProviders method [Security],ICEnroll3 interface, enumProviders method [Security],ICEnroll4 interface, security.icenroll4_enumproviders, xenroll/ICEnroll2::enumProviders, xenroll/ICEnroll3::enumProviders, xenroll/ICEnroll4::enumProviders, xenroll/ICEnroll::enumProviders
req.header: xenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Xenroll.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICEnroll::enumProviders
 - xenroll/ICEnroll::enumProviders
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Xenroll.dll
api_name:
 - ICEnroll4.enumProviders
 - ICEnroll3.enumProviders
 - ICEnroll2.enumProviders
 - ICEnroll.enumProviders
 - CEnroll.enumProviders
---

# ICEnroll::enumProviders


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>enumProviders</b> method retrieves the names of the available <a href="/windows/desktop/SecGloss/c-gly">cryptographic service providers</a> (CSPs) specified by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">ProviderType</a> property. This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a> interface.

## -parameters

### -param dwIndex [in]

Specifies the ordinal position of the CSP whose name will be retrieved. Specify zero for the first CSP.

### -param dwFlags [in]

Specifies flags that are passed through to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumprovidersa">CryptEnumProviders</a> function. This parameter is not currently used; specify zero.

### -param pbstrProvName [out]

A pointer to a <b>BSTR</b> variable that receives the name of a CSP with the specified property type. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates success. The value ERROR_NO_MORE_ITEMS is returned when there are no more CSPs with the property type indicated by the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">ProviderType</a> property.

<h3>VB</h3>
 The return value is a <b>String</b> variable that contains the name of a CSP. An exception is raised if an error is encountered or when there are no more items.

## -remarks

If the 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">ProviderType</a> property value has not been set, the default value (usually PROV_RSA_FULL) of <b>ProviderType</b> as set in the registry, is used.

The <b>enumProviders</b> method  calls the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumprovidersa">CryptEnumProviders</a> function.


#### Examples


```cpp
BSTR       bstrProvName = NULL;
DWORD      nProv;
int        j;
HRESULT    hr;

// array of CSP provider types (see Wincrypt.h)
DWORD      nProvType[] = { PROV_RSA_FULL,      
                           PROV_RSA_SIG,       
                           // list shortened for brevity
                           //...
                           PROV_STT_ISS };

// Loop, for each Prov Type.
for (j = 0; j < (sizeof(nProvType)/sizeof(DWORD)); j++)
{
    nProv = 0;
    
    // pEnroll is previously instantiated ICEnroll interface pointer
    hr = pEnroll->put_ProviderType( nProvType[j] );
    if ( FAILED(hr))
    {
        printf("Failed put_ProviderType - %x\n", hr);
        goto error;
    }
    // Enumerate the CSPs of this type.
    while ( S_OK == ( hr = pEnroll->enumProviders(nProv,
                                                  0,
                                                  &bstrProvName)))
    {
        printf("Provider %ws (type %d )\n", bstrProvName, 
            nProvType[j] );
        nProv++;
        if ( bstrProvName )
        {
            SysFreeString( bstrProvName );
            bstrProvName = NULL;
        }
    }

    // Print message if provider type does not have any CSPs.
    if ( 0 == nProv )
       printf("There were no CSPs of type %d\n", dwType );
}

error:
// Clean up resources, and so on.
if ( bstrProvName )
    SysFreeString( bstrProvName );
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll">ICEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll-get_providertype">ProviderType</a>