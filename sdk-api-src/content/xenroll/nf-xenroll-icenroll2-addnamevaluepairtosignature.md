---
UID: NF:xenroll.ICEnroll2.addNameValuePairToSignature
title: ICEnroll2::addNameValuePairToSignature (xenroll.h)
description: Adds the authenticated name-value pair of an attribute to the request. It is up to the certification authority (CA) to interpret the meaning of the name-value pair.
helpviewer_keywords: ["CEnroll object [Security]","addNameValuePairToSignature method","ICEnroll2 interface [Security]","addNameValuePairToSignature method","ICEnroll2.addNameValuePairToSignature","ICEnroll2::addNameValuePairToSignature","ICEnroll3 interface [Security]","addNameValuePairToSignature method","ICEnroll3::addNameValuePairToSignature","ICEnroll4 interface [Security]","addNameValuePairToSignature method","ICEnroll4::addNameValuePairToSignature","addNameValuePairToSignature","addNameValuePairToSignature method [Security]","addNameValuePairToSignature method [Security]","CEnroll object","addNameValuePairToSignature method [Security]","ICEnroll2 interface","addNameValuePairToSignature method [Security]","ICEnroll3 interface","addNameValuePairToSignature method [Security]","ICEnroll4 interface","security.icenroll4_addnamevaluepairtosignature","xenroll/ICEnroll2::addNameValuePairToSignature","xenroll/ICEnroll3::addNameValuePairToSignature","xenroll/ICEnroll4::addNameValuePairToSignature"]
old-location: security\icenroll4_addnamevaluepairtosignature.htm
tech.root: security
ms.assetid: a31975f7-432e-47bb-a24e-508c6ca85373
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],addNameValuePairToSignature method, ICEnroll2 interface [Security],addNameValuePairToSignature method, ICEnroll2.addNameValuePairToSignature, ICEnroll2::addNameValuePairToSignature, ICEnroll3 interface [Security],addNameValuePairToSignature method, ICEnroll3::addNameValuePairToSignature, ICEnroll4 interface [Security],addNameValuePairToSignature method, ICEnroll4::addNameValuePairToSignature, addNameValuePairToSignature, addNameValuePairToSignature method [Security], addNameValuePairToSignature method [Security],CEnroll object, addNameValuePairToSignature method [Security],ICEnroll2 interface, addNameValuePairToSignature method [Security],ICEnroll3 interface, addNameValuePairToSignature method [Security],ICEnroll4 interface, security.icenroll4_addnamevaluepairtosignature, xenroll/ICEnroll2::addNameValuePairToSignature, xenroll/ICEnroll3::addNameValuePairToSignature, xenroll/ICEnroll4::addNameValuePairToSignature
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
 - ICEnroll2::addNameValuePairToSignature
 - xenroll/ICEnroll2::addNameValuePairToSignature
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
 - ICEnroll4.addNameValuePairToSignature
 - ICEnroll3.addNameValuePairToSignature
 - ICEnroll2.addNameValuePairToSignature
 - CEnroll.addNameValuePairToSignature
---

# ICEnroll2::addNameValuePairToSignature


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>addNameValuePairToSignature</b> method 
			adds the authenticated name-value pair of an <a href="/windows/desktop/SecGloss/a-gly">attribute</a> to the request. It is up to the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA) to interpret the meaning of the name-value pair.
		 This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll2">ICEnroll2</a> interface.

## -parameters

### -param Name [in]

The name of the attribute, such as "2.5.4.6" for the country/region name.

### -param Value [in]

The value of the attribute, such as "US".

## -returns

<h3>VB</h3>
 The return value is an <b>HRESULT</b>, with <b>S_OK</b> returned if the call is successful.

## -remarks

The <b>addNameValuePairToSignature</b> method is used  to add attributes to the request.


#### Examples


```cpp
BSTR bstrName = NULL;
BSTR bstrValue = NULL;
HRESULT hr;

// Allocate the name. Alternatively, (L"2.5.4.6").
bstrName = SysAllocString(TEXT(szOID_COUNTRY_NAME));
// Allocate the value.
bstrValue = SysAllocString(L"US");

if (NULL == bstrName || NULL == bstrValue)
{
    // handle error
}

// add the name-value pair to the signature
// pEnroll is previously instantiated ICEnroll4 interface pointer
hr = pEnroll->addNameValuePairToSignature( bstrName, bstrValue );
if ( FAILED( hr ) )
    printf("Failed addNameValuePairToSignature - %x\n", hr );
else
    printf("addNameValuePairToSignature(%ws, %ws) succeeded\n",
            bstrName, 
            bstrValue );

// free BSTRs
if (bstrName )
    SysFreeString( bstrName );
if (bstrValue )
    SysFreeString( bstrValue );
```