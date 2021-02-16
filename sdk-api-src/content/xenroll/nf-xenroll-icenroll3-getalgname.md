---
UID: NF:xenroll.ICEnroll3.GetAlgName
title: ICEnroll3::GetAlgName (xenroll.h)
description: Retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current cryptographic service provider (CSP). This method was first defined in the ICEnroll3 interface.
helpviewer_keywords: ["CEnroll object [Security]","GetAlgName method","GetAlgName","GetAlgName method [Security]","GetAlgName method [Security]","CEnroll object","GetAlgName method [Security]","ICEnroll3 interface","GetAlgName method [Security]","ICEnroll4 interface","ICEnroll3 interface [Security]","GetAlgName method","ICEnroll3.GetAlgName","ICEnroll3::GetAlgName","ICEnroll4 interface [Security]","GetAlgName method","ICEnroll4::GetAlgName","security.icenroll4_getalgname","xenroll/ICEnroll3::GetAlgName","xenroll/ICEnroll4::GetAlgName"]
old-location: security\icenroll4_getalgname.htm
tech.root: security
ms.assetid: 9c5fa25c-7fab-4fb5-9ff6-bc7379260926
ms.date: 12/05/2018
ms.keywords: CEnroll object [Security],GetAlgName method, GetAlgName, GetAlgName method [Security], GetAlgName method [Security],CEnroll object, GetAlgName method [Security],ICEnroll3 interface, GetAlgName method [Security],ICEnroll4 interface, ICEnroll3 interface [Security],GetAlgName method, ICEnroll3.GetAlgName, ICEnroll3::GetAlgName, ICEnroll4 interface [Security],GetAlgName method, ICEnroll4::GetAlgName, security.icenroll4_getalgname, xenroll/ICEnroll3::GetAlgName, xenroll/ICEnroll4::GetAlgName
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
 - ICEnroll3::GetAlgName
 - xenroll/ICEnroll3::GetAlgName
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
 - ICEnroll4.GetAlgName
 - ICEnroll3.GetAlgName
 - CEnroll.GetAlgName
---

# ICEnroll3::GetAlgName


## -description

<p class="CCE_Message">[This method is no longer available for use as of Windows Server 2008 and Windows Vista.]

The <b>GetAlgName</b> method retrieves the name of a cryptographic algorithm given its ID. The values retrieved by this method depend on the current <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP). This method was first defined in the <a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a> interface.

## -parameters

### -param algID [in]

A value that represents a cryptographic algorithm, as defined in Wincrypt.h. For example, CALG_MD2 is a defined algorithm identifier. For this method to be successful, the current CSP must support the <i>algID</i> algorithm.

### -param pbstr [out]

Upon success, a pointer to a <b>BSTR</b> that represents the name of the algorithm specified by <i>algID</i>. When you have finished using the <b>BSTR</b>, free it by calling the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function.

## -returns

<h3>C++</h3>
 The return value is an <b>HRESULT</b>. A value of S_OK indicates success. If a CSP does not support this method or does not support the <i>algID</i> cryptographic algorithm, an error is returned.

<h3>VB</h3>
 The return value is a string that represents the name of the algorithm specified by <i>algID</i>. If a CSP does not support this method, an error is returned.

## -remarks

This method may be used to display the names of algorithms whose IDs are retrieved by calling 
<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll3-enumalgs">EnumAlgs</a>.

Constants for the cryptographic algorithms are defined in Wincrypt.h.


#### Examples


```cpp
BSTR      bstrAlgName = NULL;

HRESULT   hr;

// Retrieve the algorithm name.
// dwAlgID is a DWORD variable for an algorithm ID.
hr = pEnroll->GetAlgName( dwAlgID, &bstrAlgName);
if (FAILED(hr))
    printf("Failed GetAlgName [%x]\n", hr);
else
    printf("AlgID: %d Name: %S\n", dwAlgID, bstrAlgName );

// Free BSTR resource.
if ( NULL != bstrAlgName )
{
    SysFreeString( bstrAlgName );
    bstrAlgName = NULL;
}
```

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)">CEnroll</a>



<a href="/windows/desktop/api/xenroll/nf-xenroll-icenroll3-enumalgs">EnumAlgs</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll3">ICEnroll3</a>



<a href="/windows/desktop/api/xenroll/nn-xenroll-icenroll4">ICEnroll4</a>