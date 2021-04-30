---
UID: NF:xenroll.ICEnroll3.EnumAlgs
title: ICEnroll3::EnumAlgs (xenroll.h)
description: The ICEnroll4::EnumAlgs method retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current cryptographic service provider (CSP).
helpviewer_keywords: ["CEnroll object [Security]","EnumAlgs method","EnumAlgs","EnumAlgs method [Security]","EnumAlgs method [Security]","CEnroll object","EnumAlgs method [Security]","ICEnroll3 interface","EnumAlgs method [Security]","ICEnroll4 interface","ICEnroll3 interface [Security]","EnumAlgs method","ICEnroll3.EnumAlgs","ICEnroll3::EnumAlgs","ICEnroll4 interface [Security]","EnumAlgs method","ICEnroll4::EnumAlgs","security.icenroll4_enumalgs","xenroll/ICEnroll3::EnumAlgs","xenroll/ICEnroll4::EnumAlgs"]
old-location: security\icenroll4_enumalgs.htm
tech.root: security
ms.assetid: b7fe4abc-38e8-42a0-a7a0-312ccfc309e5
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],EnumAlgs method, EnumAlgs, EnumAlgs method [Security], EnumAlgs method [Security],CEnroll object, EnumAlgs method [Security],ICEnroll3 interface, EnumAlgs method [Security],ICEnroll4 interface, ICEnroll3 interface [Security],EnumAlgs method, ICEnroll3.EnumAlgs, ICEnroll3::EnumAlgs, ICEnroll4 interface [Security],EnumAlgs method, ICEnroll4::EnumAlgs, security.icenroll4_enumalgs, xenroll/ICEnroll3::EnumAlgs, xenroll/ICEnroll4::EnumAlgs
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
 - ICEnroll3::EnumAlgs
 - xenroll/ICEnroll3::EnumAlgs
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
 - ICEnroll4.EnumAlgs
 - ICEnroll3.EnumAlgs
 - CEnroll.EnumAlgs
---

# ICEnroll3::EnumAlgs


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>EnumAlgs</b> method retrieves the IDs of cryptographic algorithms in a given algorithm class that are supported by the current <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).  This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a> interface.

## -parameters

### -param dwIndex [in]

Specifies the ordinal position of the algorithm whose ID will be retrieved. Specify zero for the first algorithm.

### -param algClass [in]

A cryptographic algorithm class. The IDs returned by this method will be in the specified class. Specify one of the following:

<ul>
<li>ALG_CLASS_HASH</li>
<li>ALG_CLASS_KEY_EXCHANGE</li>
<li>ALG_CLASS_MSG_ENCRYPT</li>
<li>ALG_CLASS_DATA_ENCRYPT</li>
<li>ALG_CLASS_SIGNATURE</li>
</ul>

### -param pdwAlgID [out]

A pointer to a variable to receive a cryptographic algorithm ID that is supported by the current CSP.

## -returns

<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates success. When there are no more algorithms to enumerate, the value ERROR_NO_MORE_ITEMS is returned.

<h3>VB</h3>
 A cryptographic algorithm ID which is supported by the current CSP. When there are no more algorithms to enumerate, the value ERROR_NO_MORE_ITEMS is returned.

## -remarks

For algorithm ID and class constants used by this method, see Wincrypt.h.


#### Examples


```cpp
#include <windows.h>
#include <stdio.h>
#include <Xenroll.h>

DWORD     dwAlgID;
DWORD     dwIndex;

BSTR      bstrAlgName = NULL;

HRESULT   hr, hr2;

// Loop through the AlgIDs.
dwIndex = 0;
while ( TRUE )
{
    // Enumerate the alg IDs for a specific class.
    hr = pEnroll->EnumAlgs(dwIndex, ALG_CLASS_SIGNATURE, &dwAlgID);
    if ( S_OK != hr )
    {
       break;
    }

    // Do something with the AlgID.
    // For example, retrieve the corresponding name.
    hr2 = pEnroll->GetAlgName( dwAlgID, &bstrAlgName);
    if ( FAILED( hr2 ) )    
        printf("Failed GetAlgName [%x]\n", hr);
    else
        printf("AlgID: %d Name: %S\n", dwAlgID, bstrAlgName );

    // Reuse the BSTR variable in next iteration.
    if ( NULL != bstrAlgName )
    {
        SysFreeString( bstrAlgName );
        bstrAlgName = NULL;
    }

    // Increment the index.
    dwIndex++;
}


```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>