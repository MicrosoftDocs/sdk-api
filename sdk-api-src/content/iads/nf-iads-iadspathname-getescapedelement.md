---
UID: NF:iads.IADsPathname.GetEscapedElement
title: IADsPathname::GetEscapedElement (iads.h)
description: Used to escape special characters in the input path.
helpviewer_keywords: ["GetEscapedElement","GetEscapedElement method [ADSI]","GetEscapedElement method [ADSI]","IADsPathname interface","IADsPathname interface [ADSI]","GetEscapedElement method","IADsPathname.GetEscapedElement","IADsPathname::GetEscapedElement","_ds_iadspathname_getescapedelement","adsi.iadspathname__getescapedelement","adsi.iadspathname_getescapedelement","iads/IADsPathname::GetEscapedElement"]
old-location: adsi\iadspathname_getescapedelement.htm
tech.root: adsi
ms.assetid: a61702bd-26a8-4bd9-96c1-82a59dad7ead
ms.date: 12/05/2018
ms.keywords: GetEscapedElement, GetEscapedElement method [ADSI], GetEscapedElement method [ADSI],IADsPathname interface, IADsPathname interface [ADSI],GetEscapedElement method, IADsPathname.GetEscapedElement, IADsPathname::GetEscapedElement, _ds_iadspathname_getescapedelement, adsi.iadspathname__getescapedelement, adsi.iadspathname_getescapedelement, iads/IADsPathname::GetEscapedElement
req.header: iads.h
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsPathname::GetEscapedElement
 - iads/IADsPathname::GetEscapedElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPathname.GetEscapedElement
---

# IADsPathname::GetEscapedElement


## -description

The <b>IADsPathname::GetEscapedElement</b> method is used to escape special characters in the input path.

## -parameters

### -param lnReserved [in]

Reserved for future use.

### -param bstrInStr [in]

An input string.

### -param pbstrOutStr [out]

An output string.

## -returns

This method supports the standard return values, as well as the following:

For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

This method is used to handle a path that contains special characters in a unescaped string as input from a user interface. The input string must be a single element (name-value pair) of the path; that is, "CN=Smith,Jeff".


#### Examples

The following Visual Basic code example shows the effect produced by <b>IADsPathname::GetEscapedElement</b>. After this code is executed, rdn will contain "cn=smith\,jeff".


```vb
Dim x As New Pathname
 
rdn = x.GetEscapedElement(0, "cn=smith,jeff")
```


The following VBScript code example shows the effect produced by <b>IADsPathname::GetEscapedElement</b>. After this code is executed, rdn will contain "cn=smith\,jeff".


```vb
Dim x 
Set x = CreateObject("Pathname")
rdn = x.GetEscapedElement(0, "cn=smith,jeff")
```


The following C++ code example shows the effect produced by <b>IADsPathname::GetEscapedElement</b>. After this code is executed, rdn will contain "cn=smith\,jeff".


```cpp
LPWSTR adsPath=L"LDAP://server/cn=jeffsmith,dc=Fabrikam,dc=com";
 
IADsPathname *pPath = GetPathnameObject(adsPath);
BSTR rdn;
HRESULT hr = pPath->GetEscapedElement(0,CComBSTR("cn=smith,jeff")
                                      ,&rdn);
 
pPath->Release();
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a>