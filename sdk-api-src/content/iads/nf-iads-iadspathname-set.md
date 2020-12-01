---
UID: NF:iads.IADsPathname.Set
title: IADsPathname::Set (iads.h)
description: Sets up the Pathname object for parsing a directory path.
helpviewer_keywords: ["IADsPathname interface [ADSI]","Set method","IADsPathname.Set","IADsPathname::Set","Set","Set method [ADSI]","Set method [ADSI]","IADsPathname interface","_ds_iadspathname_set","adsi.iadspathname__set","adsi.iadspathname_set","iads/IADsPathname::Set"]
old-location: adsi\iadspathname_set.htm
tech.root: adsi
ms.assetid: 1672c1b0-1008-41e7-8ca4-eefb559f523d
ms.date: 12/05/2018
ms.keywords: IADsPathname interface [ADSI],Set method, IADsPathname.Set, IADsPathname::Set, Set, Set method [ADSI], Set method [ADSI],IADsPathname interface, _ds_iadspathname_set, adsi.iadspathname__set, adsi.iadspathname_set, iads/IADsPathname::Set
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
 - IADsPathname::Set
 - iads/IADsPathname::Set
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
 - IADsPathname.Set
---

# IADsPathname::Set


## -description

The <b>IADsPathname::Set</b> method sets up the Pathname object for parsing a directory path. The path is set with a format as defined in  <a href="/windows/win32/api/iads/ne-iads-ads_settype_enum">ADS_SETTYPE_ENUM</a>.

## -parameters

### -param bstrADsPath [in]

Path of an ADSI object.

### -param lnSetType [in]

An <a href="/windows/win32/api/iads/ne-iads-ads_settype_enum">ADS_SETTYPE_ENUM</a> option that defines the format type to be retrieved.

## -returns

This method supports the standard return values, as well as the following:

For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

This method will set the namespace as specified and identify the appropriate provider for performing the path cracking operation. Resetting to a different namespace will lose data already set by this method.


#### Examples

The following Visual Basic code example sets a full ADSI path on the Pathname object.


```vb
Dim x As New Pathname
 
x.Set "LDAP://server/CN=Jeff Smith, DC=Fabrikam, DC=Com", _
       ADS_SETTYPE_FULL
dn = x.GetElement(0)    ' dn now is "CN=Jeff Smith".
```


The following VBScript/ASP code example sets a full ADSI path on the Pathname object.


```vb
<%
Dim x
const ADS_SETTYPE_FULL = 1
Set x = CreateObject("Pathname")
path = "LDAP://server/CN=Jeff Smith, DC=Fabrikam,DC=com" 
x.Set path, ADS_SETTYPE_FULL
dn = x.GetElement(0)    ' dn now is "CN=Jeff Smith".
%>
```


The following C++ code example sets a full ADSI path on the Pathname object.


```cpp
IADsPathname *pPathname=NULL;
HRESULT hr;
 
hr = CoCreateInstance(CLSID_Pathname,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsPathname,
                      (void**)&pPathname);
 
if(FAILED(hr)) 
{
    if(pPathname) pPathname->Release();
    return NULL;
}
 
hr = pPathname->Set(CComBSTR("LDAP://CN=pencil/desk"), 
                    ADS_SETTYPE_FULL);
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/win32/api/iads/ne-iads-ads_settype_enum">ADS_SETTYPE_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspathname">IADsPathname</a>