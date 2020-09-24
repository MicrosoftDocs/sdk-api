---
UID: NF:iads.IADsPathname.CopyPath
title: IADsPathname::CopyPath (iads.h)
description: Creates a copy of the Pathname object.
helpviewer_keywords: ["CopyPath","CopyPath method [ADSI]","CopyPath method [ADSI]","IADsPathname interface","IADsPathname interface [ADSI]","CopyPath method","IADsPathname.CopyPath","IADsPathname::CopyPath","_ds_iadspathname_copypath","adsi.iadspathname__copypath","adsi.iadspathname_copypath","iads/IADsPathname::CopyPath"]
old-location: adsi\iadspathname_copypath.htm
tech.root: adsi
ms.assetid: 00c4a0b8-4961-4ceb-86fe-5cdc4e0a45c0
ms.date: 12/05/2018
ms.keywords: CopyPath, CopyPath method [ADSI], CopyPath method [ADSI],IADsPathname interface, IADsPathname interface [ADSI],CopyPath method, IADsPathname.CopyPath, IADsPathname::CopyPath, _ds_iadspathname_copypath, adsi.iadspathname__copypath, adsi.iadspathname_copypath, iads/IADsPathname::CopyPath
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
 - IADsPathname::CopyPath
 - iads/IADsPathname::CopyPath
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
 - IADsPathname.CopyPath
---

# IADsPathname::CopyPath


## -description

The <b>IADsPathname::CopyPath</b> method 
   creates a copy of the Pathname object.

## -parameters

### -param ppAdsPath [out]

The <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer on the 
      returned <a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a> object.

## -returns

This method supports the standard return values, as well as the following:

For more information and other return values, see <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error 
       Codes</a>.

## -remarks

This method is used to modify the object path and retain the original object path.


#### Examples

The following Visual Basic code example shows how to make a copy of a pathname.


```vb
Dim x, y As New Pathname
x.Set "LDAP://srv1/dc=dom,dc=company,dc=com",ADS_SETTYPE_FULL
set y = x.CopyPath
MsgBox y.Retrieve(ADS_FORMAT_WINDOWS)
```


The following VBScript/ASP code example shows how to make a copy of a pathname.


```vb
<%
Dim x, y
Const ADS_SETTYPE_FULL = 1
Const ADS_FORMAT_WINDOWS = 1
Set x = CreateObject("Pathname")
x.Set "LDAP://srv1/dc=dom,dc=company,dc=com",ADS_SETTYPE_FULL
 
set y = x.CopyPath
Response.Write y.Retrieve(ADS_FORMAT_WINDOWS)
%>
```


The following C++ code example creates a copy of a pathname object. For more information and a code example 
     of the <b>GetPathnameObject</b> function, see 
     <a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a>.


```cpp
IADsPathname *pPath;
LPWSTR adsPath;
adsPath = L"LDAP://server/cn=jeff smith,dc=Fabrikam,dc=com";
 
IADsPathname *pPath = GetPathnameObject(adsPath)
if (!pPath) exit(0);
 
IDispatch *pDisp;
HRESULT hr;
hr = pPath->CopyPath(&pDisp);
if(FAILED(hr)) exit(hr);
 
IADsPathname *pPathCopy;
hr = pDisp->QueryInterface(IID_IADsPathname,(void**)&pPathCopy);
 
// ...
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a>