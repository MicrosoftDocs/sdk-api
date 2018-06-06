---
UID: NF:iads.IADs.SetInfo
title: IADs::SetInfo
author: windows-sdk-content
description: The IADs::SetInfo method saves the cached property values of the ADSI object to the underlying directory store.
old-location: adsi\iads_setinfo.htm
old-project: ADSI
ms.assetid: e7ff6acd-b7c4-463d-a34f-fd793067c63a
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADs interface [ADSI],SetInfo method, IADs.SetInfo, IADs::SetInfo, SetInfo, SetInfo method [ADSI], SetInfo method [ADSI],IADs interface, _ds_iads_setinfo, adsi.iads__setinfo, adsi.iads_setinfo, iads/IADs::SetInfo
ms.prod: windows
ms.technology: windows-sdk
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
 - IADs.SetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADs::SetInfo


## -description


The <b>IADs::SetInfo</b> method saves the cached property values of the ADSI object to the underlying directory store.


## -parameters






## -returns



This method supports the standard return values, including S_OK for a successful operation. For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



It is important to emphasize the differences between the  <a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a> and <b>IADs::SetInfo</b> methods. The former sets (or modifies) values of a given property in the property cache whereas the latter propagates the changes from the property cache into the underlying directory store. Therefore, any property value changes made by <b>IADs::Put</b> will be lost if <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a> (or <a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a>) is invoked before <b>IADs::SetInfo</b> is called.

Because <b>IADs::SetInfo</b> sends data across networks, minimize the usage of this method. This reduces the number of trips  a client makes to the server. For example, you should commit all, or most, of the changes to the properties from the cache to the persistent store in one batch.

This guideline pertains only to the relationship of <b>IADs::SetInfo</b> with the <a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a> method, which differs from the relationship with the <a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs::PutEx</a> method.

The following code example illustrates the recommended  relation between <a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a> and <b>IADs::SetInfo</b>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim obj as IADs
 
obj.Put(prop1,val1)
obj.Put(prop2.val2)
obj.Put(prop3.val3)
obj.SetInfo</pre>
</td>
</tr>
</table></span></div>
The following code example illustrates what is not recommended between <a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a> and <b>IADs::SetInfo</b>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>obj.Put(prop1,val1)
obj.SetInfo
obj.Put(prop2.val2)
obj.SetInfo
obj.Put(prop3.val3)
obj.SetInfo</pre>
</td>
</tr>
</table></span></div>
When used with  <a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs::PutEx</a>, <b>IADs::SetInfo</b> passes the operational requests specified by control codes, such as ADS_PROPERTY_UPDATE or ADS_PROPERTY_CLEAR, to the underlying directory store.


#### Examples

The following Visual Basic code example uses the <b>IADs::SetInfo</b> method to save the property value of a user to the underlying directory.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x as IADs
On Error GoTo Cleanup

Set x = GetObject("LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com")
'
' Update values in the cache.
'
x.Put "sn", "Smith"
x.Put "givenName", "Jeff"
x.Put "street", "1 Tanka Place"
x.Put "l", "Sammamish"
x.Put "st", "Washington"
'
' Commit changes to the directory.
x.SetInfo

Cleanup:
   If (Err.Number&lt;&gt;0) Then
      MsgBox("An error has occurred. " &amp; Err.Number)
   End If
   Set x = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following C++ code example updates property values in the property cache and commits the change to the directory store using <b>IADs::SetInfo</b>. For brevity, error checking is omitted.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADs *pAds NULL;
VARIANT var;
HRESULT hr = S_OK;
LPWSTR path=L"LDAP://CN=Administrator,CN=Users,DC=Fabrikam,DC=com";
hr = ADsGetObject( path, IID_IADs, (void**) pADs);

if(!(hr==S_OK)) {return hr;}

VariantInit(&amp;var);
// Update values in the cache.
V_BSTR(&amp;var) = SysAllocString(L"Smith");
V_VT(&amp;var) = VT_BSTR;
hr = pADs-&gt;Put(CComBSTR("sn"), var );
VariantClear(&amp;var);
 
V_BSTR(&amp;var) = SysAllocString(L"Jeff");
V_VT(&amp;var) = VT_BSTR;
hr = pADs-&gt;Put(CComBSTR("givenName"), var );
VariantClear(&amp;var);
 
V_BSTR(&amp;var) = SysAllocString(L"1 Tanka Place");
V_VT(&amp;var) = VT_BSTR;
hr = pADs-&gt;Put(CComBSTR("street"), var );
VariantClear(&amp;var);
 
V_BSTR(&amp;var) = SysAllocString(L"Sammamish");
V_VT(&amp;var) = VT_BSTR;
hr = pADs-&gt;Put(CComBSTR("l"), var );
VariantClear(&amp;var);
 
V_BSTR(&amp;var) = SysAllocString(L"Washington");
V_VT(&amp;var) = VT_BSTR;
hr = pADs-&gt;Put(CComBSTR("st"), var );
VariantClear(&amp;var);
 
// Commit changes to the directory store.
hr = pADs-&gt;SetInfo();

if(pADs)
   pADs-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a>



<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a>



<a href="https://msdn.microsoft.com/fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7">IADs::PutEx</a>
 

 

