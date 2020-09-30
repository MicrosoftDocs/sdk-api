---
UID: NF:iads.IADsNameTranslate.SetEx
title: IADsNameTranslate::SetEx (iads.h)
description: Establishes an array of objects for name translation.
helpviewer_keywords: ["IADsNameTranslate interface [ADSI]","SetEx method","IADsNameTranslate.SetEx","IADsNameTranslate::SetEx","SetEx","SetEx method [ADSI]","SetEx method [ADSI]","IADsNameTranslate interface","_ds_iadsnametranslate_setex","adsi.iadsnametranslate__setex","adsi.iadsnametranslate_setex","iads/IADsNameTranslate::SetEx"]
old-location: adsi\iadsnametranslate_setex.htm
tech.root: adsi
ms.assetid: e8a5014e-d848-46b7-a336-7801ff1f6b08
ms.date: 12/05/2018
ms.keywords: IADsNameTranslate interface [ADSI],SetEx method, IADsNameTranslate.SetEx, IADsNameTranslate::SetEx, SetEx, SetEx method [ADSI], SetEx method [ADSI],IADsNameTranslate interface, _ds_iadsnametranslate_setex, adsi.iadsnametranslate__setex, adsi.iadsnametranslate_setex, iads/IADsNameTranslate::SetEx
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
 - IADsNameTranslate::SetEx
 - iads/IADsNameTranslate::SetEx
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
 - IADsNameTranslate.SetEx
---

# IADsNameTranslate::SetEx


## -description

The <b>IADsNameTranslate::SetEx</b> method establishes an array of objects for name translation. The specified objects must exist in the connected directory server. To set the name and format of a single directory object, use the  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-set">IADsNameTranslate::Set</a> method.

## -parameters

### -param lnFormatType

The format type of the input names. For more information, see  <a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a>.

### -param pvar

A variant array of strings that hold object names.

## -returns

This method supports the standard <b>HRESULT</b> return values, including:

## -remarks

You cannot use the <b>IADsNameTranslate::SetEx</b> method to set name translation for objects residing on other servers, even when the referral chasing option is enabled. For more information about referral chasing, see  <a href="/windows/desktop/ADSI/iadsnametranslate-property-methods">IADsNameTranslate Property Methods</a>.

You can use <b>IADsNameTranslate::SetEx</b> to set names for multiple objects. All the names, however, must be of the same format.


#### Examples

The following C/C++ code example uses the <b>IADsNameTranslate::SetEx</b> method to set up an array of objects whose names are to be translated from the RFC 1779 format to the Windows user name format.


```cpp
IADsNameTranslate *pNto;
HRESULT hr;
hr = CoCreateInstance(CLSID_NameTranslate,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsNameTranslate,
                      (void**)&pNto);
if(FAILED(hr)) { exit 1;}
 
hr = pNto->Init(ADS_NAME_INITTYPE_SERVER,
                  CComBSTR("myServer"));
if (FAILED(hr)) { exit 1;}
 
LPWSTR str[1] = { L"CN=jim,CN=Users,DC=myDomain,DC=Fabrikam,DC=COM",
                  L"CN=rob,CN=Users,DC=myDomain,DC=Fabrikam,DC=COM"};
DWORD dwNum = sizeof(str)/sizeof(LPWSTR);
 
VARIANT varStr;
VariantInit(&varStr);
 
hr = ADsBuildVarArrayStr(str,dwNum,&varStr);
 
hr =pNto->SetEx(ADS_NAME_TYPE_1779, varStr);
if(FAILED(hr)) {exit 1;}
VariantClear(&varStr);
 
hr = pNto->GetEx(ADS_NAME_TYPE_GUID, &varStr);
if(FAILED(hr)) {exit 1;}
 
LONG lstart, lend;
SAFEARRAY *sa = V_ARRAY(&varStr);
VARIANT varItem;
VariantInit(&varItem);
printf("Names in the translated format:\n");
for (long idx = lstart; idx <= lend; idx++) 
{
    hr = SafeArrayGetElement(sa, &idx, &varItem);
    printf("   %S\n", V_BSTR(&varItem));
    VariantClear(&varItem);
}
VariantClear(&varStr);
pNto->Release();
```


The following Visual Basic code example uses the <b>IADsNameTranslate::SetEx</b> method to set up an array of objects whose names are to be translated from the RFC 1779 format to the s user name format.


```vb
Dim nto As New NameTranslate
dso(0)="CN=jeffSmith, CN=users, DC=Fabrikam dc=COM"
dso(1)="CN=brendaDiaz, CN=users, DC=Fabrikam dc=COM"
nto.Init  ADS_NAME_INITTYPE_SERVER, "myServer"
nto.SetEx ADS_NAME_TYPE_1779, dso
trans = nto.GetEx(ADS_NAME_TYPE_NT4)   
Msgbox "Translations: " & trans(0) & "," & trans(1)
```


The following VBScript/ASP code example uses the <b>IADsNameTranslate::SetEx</b> method to set up an array of objects whose names are to be translated from the RFC 1779 format to the s user name format.


```vb
<%@ Language=VBScript %>
<html>
<body>
<%
  Dim nto
  const ADS_NAME_INITTYPE_SERVER = 2  ' VBScript cannot read 
  const ADS_NAME_TYPE_1779 = 1        ' enumeration definition
  const ADS_NAME_TYPE_NT4 = 3
 
  dn(0) = "CN=jeffSmith,CN=Users,DC=Fabrikam,DC=COM" 
  dn(1) = "CN=brendaDiaz,CN=Users,DC=Fabrikam,DC=COM" 
 
  Set nto = Server.CreateObject("NameTranslate")
  nto.Init ADS_NAME_INITTYPE_SERVER, "myServer"
  nto.SetEx ADS_NAME_TYPE_1779, dn
  result = nto.GetEx(ADS_NAME_TYPE_NT4)
 
  Response.Write "<p>Name in the translated format: " & result(0) & _
       ", & result(1)
 
%>
</body>
</html>
```

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a>



<a href="/windows/desktop/ADSI/iadsnametranslate-property-methods">IADsNameTranslate Property Methods</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-set">IADsNameTranslate::Set</a>