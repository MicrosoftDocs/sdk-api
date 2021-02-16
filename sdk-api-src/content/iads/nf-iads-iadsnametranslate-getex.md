---
UID: NF:iads.IADsNameTranslate.GetEx
title: IADsNameTranslate::GetEx (iads.h)
description: Gets the object names in the specified format.
helpviewer_keywords: ["GetEx","GetEx method [ADSI]","GetEx method [ADSI]","IADsNameTranslate interface","IADsNameTranslate interface [ADSI]","GetEx method","IADsNameTranslate.GetEx","IADsNameTranslate::GetEx","_ds_iadsnametranslate_getex","adsi.iadsnametranslate__getex","adsi.iadsnametranslate_getex","iads/IADsNameTranslate::GetEx"]
old-location: adsi\iadsnametranslate_getex.htm
tech.root: adsi
ms.assetid: 01c4fc79-ed5b-4a24-9b97-25b4095a9c8f
ms.date: 12/05/2018
ms.keywords: GetEx, GetEx method [ADSI], GetEx method [ADSI],IADsNameTranslate interface, IADsNameTranslate interface [ADSI],GetEx method, IADsNameTranslate.GetEx, IADsNameTranslate::GetEx, _ds_iadsnametranslate_getex, adsi.iadsnametranslate__getex, adsi.iadsnametranslate_getex, iads/IADsNameTranslate::GetEx
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
 - IADsNameTranslate::GetEx
 - iads/IADsNameTranslate::GetEx
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
 - IADsNameTranslate.GetEx
---

# IADsNameTranslate::GetEx


## -description

The <b>IADsNameTranslate::GetEx</b> method gets the object names in the specified format. The  object names must be set by  <a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate::SetEx</a>.

## -parameters

### -param lnFormatType

The format type used for  the output names. For more information about the various types of formats you can use, see  <a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a>. This method does not support the ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME element in <b>ADS_NAME_TYPE_ENUM</b>.

### -param pvar

A variant array of strings that hold names of the objects returned.

## -returns

This method supports the standard <b>HRESULT</b> return values, including:

## -remarks

This method gets the names of multiple objects. However, all of the  names returned use a single format.

When referral chasing is on, this method will not attempt to chase and resolve the path of a specified object not residing on the connected server.


#### Examples

The following C/C++ code  example shows how to translate a distinguished names that is compliant with RFC 1779 to the GUID format. The computer name of the directory server is "myServer".


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


The following code example shows how to convert multiple names from the RFC 1779 type to the GUID type. The computer name of the directory server is "myServer".


```vb
Dim nto As new NameTranslate
Dim result As Variant
Dim ns(1) As String
 
nto.Init ADS_NAME_INITTTYPE_SERVER, "myServer"
 
ns(0)="CN=rob,CN=users,DC=example,DC=Fabrikam,DC=COM,O=Internet"
ns(1)="CN=jim,CN=users,DC=example,DC=Fabrikam,DC=COM,O=Internet"
 
nto.SetEx ADS_NAME_TYPE_1779, ns
nto.GetEx ADS_NAME_TYPE_GUID, result
MsgBox "name(0): " & result(0) & " name(1): " & result(1)
```


The following VBScript/ASP code example translates two distinguished names compliant with RFC 1779 to the GUID format. The computer name of the directory server is "myServer".


```vb
<%@ Language=VBScript %>
<html>
<body>
<%
  Dim nto
  const ADS_NAME_INITTYPE_SERVER = 2
  const ADS_NAME_TYPE_1779 = 1
  const ADS_NAME_TYPE_NT4 = 3
 
  server = "myServer"
  user   = "jeffsmith"
  dom    = "Fabrikam"
  passwd = "top secret" 
 
  Set nto = Server.CreateObject("NameTranslate")
  nto.InitEx ADS_NAME_INITTYPE_SERVER, server, user, dom, passwd
 
  ns(0)="CN=rob,CN=users,DC=example,DC=Fabrikam,DC=COM,O=Internet"
  ns(1)="CN=jim,CN=users,DC=example,DC=Fabrikam,DC=COM,O=Internet"
 
  nto.SetEx ADS_NAME_TYPE_1779, ns
  result = nto.GetEx(ADS_NAME_TYPE_GUID)
 
  Response.Write "<p>Names in the translated format: " & result(0) & _
    ", " & result(1)
 
%>
</body>
</html>
```

## -see-also

<a href="/windows/win32/api/iads/ne-iads-ads_name_type_enum">ADS_NAME_TYPE_ENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsnametranslate">IADsNameTranslate</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsnametranslate-setex">IADsNameTranslate::SetEx</a>