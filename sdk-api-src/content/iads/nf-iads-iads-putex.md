---
UID: NF:iads.IADs.PutEx
title: IADs::PutEx
author: windows-driver-content
description: Modifies the values of an attribute in the ADSI attribute cache.
old-location: adsi\iads_putex.htm
old-project: ADSI
ms.assetid: fb9d9b2c-9efc-4462-ac4b-9a2fbf0b5ec7
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IADs interface [ADSI],PutEx method, IADs.PutEx, IADs::PutEx, PutEx, PutEx method [ADSI], PutEx method [ADSI],IADs interface, _ds_iads_putex, adsi.iads__putex, adsi.iads_putex, iads/IADs::PutEx
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
-	IADs.PutEx
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADs::PutEx


## -description


The <b>IADs::PutEx</b> method modifies the values of an attribute in the ADSI attribute cache.  For example, for properties that allow multiple values, you can append additional values to an existing set of values, modify the values in the set, remove specified values from the set, or delete values from the set.


## -parameters




### -param lnControlCode [in]

Control code that  indicates the mode of modification: Append, Replace, Remove, and Delete. For more information and a list of values, see  <a href="https://msdn.microsoft.com/fba20292-870d-4948-abf1-225b1230e938">ADS_PROPERTY_OPERATION_ENUM</a>.


### -param bstrName [in]

Contains a <b>BSTR</b> that specifies the property name.


### -param vProp [in]

Contains a <b>VARIANT</b> array that contains the new value or values of the property. A single-valued property is represented as an array with a single element. If <i>InControlCode</i> is set to <b>ADS_PROPERTY_CLEAR</b>, the value of the property specified by <i>vProp</i> is irrelevant.


## -returns



This method supports  standard return values, as well as the following.
      

For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



<b>PutEx</b> is usually used to set values on multi-value attributes. Unlike the <a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a> method, with <b>PutEx</b>, you are not required to get the attribute values before you modify them. However, because <b>PutEx</b> only makes changes to attributes values contained in the ADSI property cache, you must use <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a> after each <b>PutEx</b> call in order to commit changes to the directory.

<b>PutEx</b> enables you to append values to an existing set of values in a multi-value attribute using <b>ADS_PROPERTY_APPEND</b>. When you update, append, or delete values to a multi-value attribute, you must use an array.

Active Directory does not accept duplicate values on a multi-valued attribute. If you call <b>PutEx</b> to append a duplicate value to a multi-valued attribute of an Active  Directory object, the <b>PutEx</b> call succeeds, but the duplicate value is ignored.

Similarly, if you use <b>PutEx</b> to delete one or more values from a multi-valued property of an Active Directory object, the operation succeeds, that is, it will not produce an error, even if any or all of the specified values are not set on the property.

<div class="alert"><b>Note</b>  The WinNT provider ignores the value passed by the <i>InControlCode</i> argument and performs the equivalent of an <b>ADS_PROPERTY_UPDATE</b> request when using <b>PutEx</b>.</div>
<div> </div>

#### Examples

The following code example shows how to use the <b>IADs.PutEx</b> method.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim x As IADs

On Error GoTo Cleanup

Set x = GetObject("LDAP://CN=JeffSmith,CN=Users,DC=Fabrikam,DC=com")
'----------------------------------------------------------
' Assume the otherHomePhone has the values
' 425-707-9790, 425-707-9791
'----------------------------------------------------------
 
' Adding a value
x.PutEx ADS_PROPERTY_APPEND, "otherhomePhone", Array("425-707-9792")  
x.SetInfo              ' Now the values are 425-707-9790,425-707-9791,425-707-9792. 
deleting two values
x.PutEx ADS_PROPERTY_DELETE, "otherHomePhone", Array("425-707-9790", "425-707-9791")
x.SetInfo              ' Now the values are 425-707-9792.
 
' Changing the remaining value
x.PutEx ADS_PROPERTY_UPDATE, "otherHomePhone", Array("425-707-9793", "425-707-9794")
x.SetInfo              ' Now the values are 425-707-9793,425-707-9794.
 
' Deleting the value
x.PutEx ADS_PROPERTY_CLEAR, "otherHomePhone",  vbNullString
x.SetInfo              ' Now the property has no value.

Cleanup:
    If(Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set x = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to use the <b>IADs::PutEx</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT hr;
IADs *pADs=NULL;
LPWSTR pszADsPath = L"LDAP://CN=JeffSmith,CN=Users,DC=Fabrikam,DC=com";
 
CoInitialize(NULL);
 
hr = ADsGetObject(pszADsPath, IID_IADs, (void**) &amp;pADs);

if(SUCCEEDED(hr)) 
{
    VARIANT var;
    VariantInit(&amp;var);
     
    LPWSTR pszPhones[] = { L"425-707-9790", L"425-707-9791" };
    DWORD dwNumber = sizeof(pszPhones)/sizeof(LPWSTR);
    hr = ADsBuildVarArrayStr(pszPhones, dwNumber, &amp;var);
    hr = pADs-&gt;Put(CComBSTR("otherHomePhone"), var); 
    VariantClear(&amp;var);
    hr = pADs-&gt;SetInfo();   // The phone list is now 425-707-9790, 425-707-9791.
     
    // Append another number to the list.
    LPWSTR pszAddPhones[]={L"425-707-9792"};
    hr = ADsBuildVarArrayStr(pszAddPhones, 1, &amp;var);
    hr = pADs-&gt;PutEx(ADS_PROPERTY_APPEND, CComBSTR("otherHomePhone"), var);
    hr = pADs-&gt;SetInfo();   // The list becomes 
                            // 425-707-9790, 425-707-9791, 425-707-9792.
    VariantClear(&amp;var);
     
    hr = ADsBuildVarArrayStr(pszPhones, dwNumber, &amp;var);
    hr = pADs-&gt;PutEx(ADS_PROPERTY_DELETE, CComBSTR("otherHomePhone"), var);
    hr = pADs-&gt;SetInfo();  // The list becomes 425-707-9792.
     
    pszPhones[0] = L"425-707-9793";
    pszPhones[1] = L"425-707-9794";
    hr = ADsBuildVarArrayStr(pszPhones, dwNumber, &amp;var);
    hr = pADs-&gt;PutEx(ADS_PROPERTY_UPDATE, CComBSTR("otherHomePhone"), var);
    hr = pADs-&gt;SetInfo();  // The list becomes 425-707-9793, 425-707-9794.
     
    VariantClear(&amp;var);
    V_VT(&amp;var)=VT_NULL;
    hr = pADs-&gt;PutEx(ADS_PROPERTY_CLEAR, CComBSTR("otherHomePhone"), var);
    hr = pADs-&gt;SetInfo();  // The list is empty.

    VariantClear(&amp;var);
    pADs-&gt;Release();
}

hr = CoUninitialize();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/f53d9ee0-3f4d-4a01-b953-98d168ad94cb">IADs</a>



<a href="https://msdn.microsoft.com/fd6d79b6-46f8-42dd-8525-a72a6e0a7672">IADs::Get</a>



<a href="https://msdn.microsoft.com/cda6b8e7-fadc-4e0b-8217-66b37bf7efbd">IADs::GetEx</a>



<a href="https://msdn.microsoft.com/b543220d-939b-4ca5-9a27-90b04f14be5d">IADs::Put</a>



<a href="https://msdn.microsoft.com/b3479719-b5bf-4f19-91f9-b05e60bde161">Property
  Cache</a>
 

 

