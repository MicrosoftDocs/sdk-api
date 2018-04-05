---
UID: NF:iads.IADsNameTranslate.SetEx
title: IADsNameTranslate::SetEx method
author: windows-driver-content
description: Establishes an array of objects for name translation.
old-location: adsi\iadsnametranslate_setex.htm
old-project: ADSI
ms.assetid: e8a5014e-d848-46b7-a336-7801ff1f6b08
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IADsNameTranslate, IADsNameTranslate interface [ADSI], SetEx method, IADsNameTranslate::SetEx, SetEx method [ADSI], SetEx method [ADSI], IADsNameTranslate interface, SetEx,IADsNameTranslate.SetEx, _ds_iadsnametranslate_setex, adsi.iadsnametranslate__setex, adsi.iadsnametranslate_setex, iads/IADsNameTranslate::SetEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Activeds.dll
api_name:
-	IADsNameTranslate.SetEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsNameTranslate::SetEx method


## -description


The <b>IADsNameTranslate::SetEx</b> method establishes an array of objects for name translation. The specified objects must exist in the connected directory server. To set the name and format of a single directory object, use the  <a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a> method.


## -parameters




### -param lnFormatType

The format type of the input names. For more information, see  <a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>.


### -param pvar






#### - pVar

A variant array of strings that hold object names.


## -returns



This method supports the standard <b>HRESULT</b> return values, including:




## -remarks



You cannot use the <b>IADsNameTranslate::SetEx</b> method to set name translation for objects residing on other servers, even when the referral chasing option is enabled. For more information about referral chasing, see  <a href="https://msdn.microsoft.com/7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc">IADsNameTranslate Property Methods</a>.

You can use <b>IADsNameTranslate::SetEx</b> to set names for multiple objects. All the names, however, must be of the same format.


#### Examples

The following C/C++ code example uses the <b>IADsNameTranslate::SetEx</b> method to set up an array of objects whose names are to be translated from the RFC 1779 format to the Windows user name format.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsNameTranslate *pNto;
HRESULT hr;
hr = CoCreateInstance(CLSID_NameTranslate,
                      NULL,
                      CLSCTX_INPROC_SERVER,
                      IID_IADsNameTranslate,
                      (void**)&amp;pNto);
if(FAILED(hr)) { exit 1;}
 
hr = pNto-&gt;Init(ADS_NAME_INITTYPE_SERVER,
                  CComBSTR("myServer"));
if (FAILED(hr)) { exit 1;}
 
LPWSTR str[1] = { L"CN=jim,CN=Users,DC=myDomain,DC=Fabrikam,DC=COM",
                  L"CN=rob,CN=Users,DC=myDomain,DC=Fabrikam,DC=COM"};
DWORD dwNum = sizeof(str)/sizeof(LPWSTR);
 
VARIANT varStr;
VariantInit(&amp;varStr);
 
hr = ADsBuildVarArrayStr(str,dwNum,&amp;varStr);
 
hr =pNto-&gt;SetEx(ADS_NAME_TYPE_1779, varStr);
if(FAILED(hr)) {exit 1;}
VariantClear(&amp;varStr);
 
hr = pNto-&gt;GetEx(ADS_NAME_TYPE_GUID, &amp;varStr);
if(FAILED(hr)) {exit 1;}
 
LONG lstart, lend;
SAFEARRAY *sa = V_ARRAY(&amp;varStr);
VARIANT varItem;
VariantInit(&amp;varItem);
printf("Names in the translated format:\n");
for (long idx = lstart; idx &lt;= lend; idx++) 
{
    hr = SafeArrayGetElement(sa, &amp;idx, &amp;varItem);
    printf("   %S\n", V_BSTR(&amp;varItem));
    VariantClear(&amp;varItem);
}
VariantClear(&amp;varStr);
pNto-&gt;Release();</pre>
</td>
</tr>
</table></span></div>
The following Visual Basic code example uses the <b>IADsNameTranslate::SetEx</b> method to set up an array of objects whose names are to be translated from the RFC 1779 format to the s user name format.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim nto As New NameTranslate
dso(0)="CN=jeffSmith, CN=users, DC=Fabrikam dc=COM"
dso(1)="CN=brendaDiaz, CN=users, DC=Fabrikam dc=COM"
nto.Init  ADS_NAME_INITTYPE_SERVER, "myServer"
nto.SetEx ADS_NAME_TYPE_1779, dso
trans = nto.GetEx(ADS_NAME_TYPE_NT4)   
Msgbox "Translations: " &amp; trans(0) &amp; "," &amp; trans(1)</pre>
</td>
</tr>
</table></span></div>
The following VBScript/ASP code example uses the <b>IADsNameTranslate::SetEx</b> method to set up an array of objects whose names are to be translated from the RFC 1779 format to the s user name format.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>&lt;%@ Language=VBScript %&gt;
&lt;html&gt;
&lt;body&gt;
&lt;%
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
 
  Response.Write "&lt;p&gt;Name in the translated format: " &amp; result(0) &amp; _
       ", &amp; result(1)
 
%&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>



<a href="https://msdn.microsoft.com/7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc">IADsNameTranslate Property Methods</a>



<a href="https://msdn.microsoft.com/1c126333-3d5c-4ba3-8c66-de778e26488f">IADsNameTranslate::Set</a>
 

 

