---
UID: NF:dsclient.IDsDisplaySpecifier.GetDisplaySpecifier
title: IDsDisplaySpecifier::GetDisplaySpecifier (dsclient.h)
description: The IDsDisplaySpecifier::GetDisplaySpecifier method binds to the display specifier object for a given class in Active Directory Domain Services.
helpviewer_keywords: ["GetDisplaySpecifier","GetDisplaySpecifier method [Active Directory]","GetDisplaySpecifier method [Active Directory]","IDsDisplaySpecifier interface","IDsDisplaySpecifier interface [Active Directory]","GetDisplaySpecifier method","IDsDisplaySpecifier.GetDisplaySpecifier","IDsDisplaySpecifier::GetDisplaySpecifier","_glines_idsdisplayspecifier_getdisplayspecifier","ad.idsdisplayspecifier__getdisplayspecifier","ad.idsdisplayspecifier_getdisplayspecifier","dsclient/IDsDisplaySpecifier::GetDisplaySpecifier"]
old-location: ad\idsdisplayspecifier_getdisplayspecifier.htm
tech.root: ad
ms.assetid: c4fc25f6-0157-406d-b523-8542183291ed
ms.date: 12/05/2018
ms.keywords: GetDisplaySpecifier, GetDisplaySpecifier method [Active Directory], GetDisplaySpecifier method [Active Directory],IDsDisplaySpecifier interface, IDsDisplaySpecifier interface [Active Directory],GetDisplaySpecifier method, IDsDisplaySpecifier.GetDisplaySpecifier, IDsDisplaySpecifier::GetDisplaySpecifier, _glines_idsdisplayspecifier_getdisplayspecifier, ad.idsdisplayspecifier__getdisplayspecifier, ad.idsdisplayspecifier_getdisplayspecifier, dsclient/IDsDisplaySpecifier::GetDisplaySpecifier
req.header: dsclient.h
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
req.lib: 
req.dll: Dsadmin.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDsDisplaySpecifier::GetDisplaySpecifier
 - dsclient/IDsDisplaySpecifier::GetDisplaySpecifier
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dsadmin.dll
api_name:
 - IDsDisplaySpecifier.GetDisplaySpecifier
---

# IDsDisplaySpecifier::GetDisplaySpecifier


## -description

The <b>IDsDisplaySpecifier::GetDisplaySpecifier</b> method binds to the display specifier object for a given class in Active Directory Domain Services.

## -parameters

### -param pszObjectClass [in]

Pointer to a null-terminated Unicode string that contains the name of the object class to retrieve the display specifier   for.

### -param riid [in]

Contains the interface identifier of the desired interface.

### -param ppv [in, out]

Pointer to an interface pointer that receives the display specifier of the object class.

## -returns

Returns a standard <b>HRESULT</b> value including the following.

## -remarks

This method uses the 
<a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a> function to bind to the display specifier object of the given class. If that fails, it attempts to bind to the display specifier in the user locale. If this fails again, it binds to the display specifier in the default locale.

This method uses the server and user credentials set by a previous call to 
<a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-setserver">IDsDisplaySpecifier::SetServer</a>.


#### Examples

The following code example demonstrates how to call this method.


```cpp
HRESULT hr;
IDsDisplaySpecifier *pDS;

hr = CoCreateInstance(CLSID_DsDisplaySpecifier,
                        NULL,
                        CLSCTX_INPROC_SERVER,
                        IID_IDsDisplaySpecifier,
                        (void**)&pDS);
if(SUCCEEDED(hr))
{
    IADs *pads;

    hr = pDS->GetDisplaySpecifier(L"user", IID_IADs, (LPVOID*)&pads);

    if(SUCCEEDED(hr))
    {
        pads->Release();
    }

    pDS->Release();
}

```

## -see-also

<a href="/windows/desktop/api/adshlp/nf-adshlp-adsopenobject">ADsOpenObject</a>



<a href="/windows/desktop/AD/display-interfaces-in-active-directory-domain-services">Display Interfaces in Active Directory Domain Services</a>



<a href="/windows/desktop/api/dsclient/nn-dsclient-idsdisplayspecifier">IDsDisplaySpecifier</a>



<a href="/windows/desktop/api/dsclient/nf-dsclient-idsdisplayspecifier-setserver">IDsDisplaySpecifier::SetServer</a>