---
UID: NF:iads.IADsNameTranslate.Set
title: IADsNameTranslate::Set
author: windows-sdk-content
description: Directs the directory service to set up a specified object for name translation.
old-location: adsi\iadsnametranslate_set.htm
old-project: ADSI
ms.assetid: 1c126333-3d5c-4ba3-8c66-de778e26488f
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IADsNameTranslate interface [ADSI],Set method, IADsNameTranslate.Set, IADsNameTranslate::Set, Set, Set method [ADSI], Set method [ADSI],IADsNameTranslate interface, _ds_iadsnametranslate_set, adsi.iadsnametranslate__set, adsi.iadsnametranslate_set, iads/IADsNameTranslate::Set
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: iads.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsNameTranslate.Set
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsNameTranslate::Set


## -description


The <b>IADsNameTranslate::Set</b> method directs the directory service to set up a specified object for name translation. To set the names and format of multiple objects, use  <a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsnametranslate::SetEx</a>.


## -parameters




### -param lnSetType

The format of the name of a directory object. For more information, see  <a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>.


### -param bstrADsPath

The object name, for example, "CN=Administrator, CN=users, DC=Fabrikam, DC=com".


## -returns



This method supports the standard <b>HRESULT</b> return values, including:




## -remarks



Before calling this method to set the object name, you should have established a connection to the directory service using either  <a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a> or  <a href="https://msdn.microsoft.com/169e1e0d-26c0-484d-b461-8817d37d17b8">IADsNameTranslate::InitEx</a>.

You can use the <b>IADsNameTranslate::Set</b> method to set name translation for objects residing on the directory server. When the referral chasing is on, this method will also set any object found on other servers. For more information about referral chasing, see  <a href="https://msdn.microsoft.com/7c44fe9b-16a5-4bd5-a80b-8f3dcfec20cc">IADsNameTranslate Property Methods</a>.


#### Examples

The following C/C++ code example uses the <b>IADsNameTranslate::Set</b> method to set an object so that its name can be translated from the RFC 1779 format to the s user name format.

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
 
hr =pNto-&gt;Set(ADS_NAME_TYPE_1779,
             CComBSTR("cn=jeffsmith,cn=users,dc=Fabrikam,dc=com"));
if(FAILED(hr)) {exit 1;}
 
BSTR bstr;
hr = pNto-&gt;Get(ADS_NAME_TYPE_NT4, &amp;bstr);
printf("Name in the translated format: %S\n", bstr);
 
SysFreeString(bstr);
pNto-&gt;Release();</pre>
</td>
</tr>
</table></span></div>
The following Visual Basic code example uses the <b>IADsNameTranslate::Set</b> method to set an object so that its name can be translated from the RFC 1779 format to the s user name format.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim nto As New NameTranslate
dso="CN=jeffsmith, CN=users, DC=Fabrikam dc=COM"
 
nto.Init ADS_NAME_INITTYPE_SERVER, "myServer"
nto.Set ADS_NAME_TYPE_1779, dso
trans = nto.Get(ADS_NAME_TYPE_NT4)  </pre>
</td>
</tr>
</table></span></div>
The following VBScript/ASP code example uses the <b>IADsNameTranslate::Set</b> method to set an object to have its name translated from the RFC 1779 format to the s user name format.

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
 
  dn = "CN=jeffsmith,CN=Users,DC=Fabrikam,DC=COM" 
 
  Set nto = Server.CreateObject("NameTranslate")
  nto.Init ADS_NAME_INITTYPE_SERVER, "myServer"
  nto.Set ADS_NAME_TYPE_1779, dn
  result = nto.Get(ADS_NAME_TYPE_NT4)
 
  Response.Write "&lt;p&gt;Name in the translated format: " &amp; result
 
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



<a href="https://msdn.microsoft.com/dad31301-b18b-44ec-b32f-93d0bb5b6189">IADsNameTranslate::Init</a>



<a href="https://msdn.microsoft.com/169e1e0d-26c0-484d-b461-8817d37d17b8">IADsNameTranslate::InitEx</a>



<a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate::SetEx</a>
 

 

