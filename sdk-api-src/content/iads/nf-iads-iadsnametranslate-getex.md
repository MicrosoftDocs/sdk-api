---
UID: NF:iads.IADsNameTranslate.GetEx
title: IADsNameTranslate::GetEx
author: windows-sdk-content
description: Gets the object names in the specified format.
old-location: adsi\iadsnametranslate_getex.htm
tech.root: ADSI
ms.assetid: 01c4fc79-ed5b-4a24-9b97-25b4095a9c8f
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetEx, GetEx method [ADSI], GetEx method [ADSI],IADsNameTranslate interface, IADsNameTranslate interface [ADSI],GetEx method, IADsNameTranslate.GetEx, IADsNameTranslate::GetEx, _ds_iadsnametranslate_getex, adsi.iadsnametranslate__getex, adsi.iadsnametranslate_getex, iads/IADsNameTranslate::GetEx
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
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsNameTranslate.GetEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- iads.h
: 
- IADsNameTranslate.GetEx
: 
---

# IADsNameTranslate::GetEx


## -description


The <b>IADsNameTranslate::GetEx</b> method gets the object names in the specified format. The  object names must be set by  <a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate::SetEx</a>.


## -parameters




### -param lnFormatType

The format type used for  the output names. For more information about the various types of formats you can use, see  <a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>. This method does not support the ADS_NAME_TYPE_SID_OR_SID_HISTORY_NAME element in <b>ADS_NAME_TYPE_ENUM</b>.


### -param pvar

TBD




#### - pVarStr

A variant array of strings that hold names of the objects returned.


## -returns



This method supports the standard <b>HRESULT</b> return values, including:




## -remarks



This method gets the names of multiple objects. However, all of the  names returned use a single format.

When referral chasing is on, this method will not attempt to chase and resolve the path of a specified object not residing on the connected server.


#### Examples

The following C/C++ code  example shows how to translate a distinguished names that is compliant with RFC 1779 to the GUID format. The computer name of the directory server is "myServer".

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
The following code example shows how to convert multiple names from the RFC 1779 type to the GUID type. The computer name of the directory server is "myServer".

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim nto As new NameTranslate
Dim result As Variant
Dim ns(1) As String
 
nto.Init ADS_NAME_INITTTYPE_SERVER, "myServer"
 
ns(0)="CN=rob,CN=users,DC=example,DC=Fabrikam,DC=COM,O=Internet"
ns(1)="CN=jim,CN=users,DC=example,DC=Fabrikam,DC=COM,O=Internet"
 
nto.SetEx ADS_NAME_TYPE_1779, ns
nto.GetEx ADS_NAME_TYPE_GUID, result
MsgBox "name(0): " &amp; result(0) &amp; " name(1): " &amp; result(1)</pre>
</td>
</tr>
</table></span></div>
The following VBScript/ASP code example translates two distinguished names compliant with RFC 1779 to the GUID format. The computer name of the directory server is "myServer".

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
 
  Response.Write "&lt;p&gt;Names in the translated format: " &amp; result(0) &amp; _
    ", " &amp; result(1)
 
%&gt;
&lt;/body&gt;
&lt;/html&gt;</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/8c5e8f2a-e805-463e-9583-96732d70b209">ADS_NAME_TYPE_ENUM</a>



<a href="https://msdn.microsoft.com/3d8baeb1-0edc-4648-8691-6ea4dcfd8f62">IADsNameTranslate</a>



<a href="https://msdn.microsoft.com/e8a5014e-d848-46b7-a336-7801ff1f6b08">IADsNameTranslate::SetEx</a>
 

 

