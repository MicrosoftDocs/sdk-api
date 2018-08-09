---
UID: NF:iads.IADsPropertyValue.Clear
title: IADsPropertyValue::Clear
author: windows-sdk-content
description: Clears the current values of the property value object.
old-location: adsi\iadspropertyvalue_clear.htm
old-project: ADSI
ms.assetid: 1662f507-6e1c-4f44-a40d-0eccd8091c51
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: Clear, Clear method [ADSI], Clear method [ADSI],IADsPropertyValue interface, IADsPropertyValue interface [ADSI],Clear method, IADsPropertyValue.Clear, IADsPropertyValue::Clear, _ds_iadspropertyvalue_clear, adsi.iadspropertyvalue__clear, adsi.iadspropertyvalue_clear, iads/IADsPropertyValue::Clear
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
 - IADsPropertyValue.Clear
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsPropertyValue::Clear


## -description


The <b>IADsPropertyValue::Clear</b> method clears the current values of the property value object.


## -parameters






## -returns



This method supports the standard HRESULT return values, including S_OK. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



None


#### Examples

The following code example shows how to use <b>IADsPropertyValue::Clear</b> to clear the value of the "description" property from a property list.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

On Error GoTo Cleanup
 
' Get the property list.
Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
' Get a property entry. If you know the exact type of the property,
' replace ADSTYPE_UNKNOWN with that type.
Set propEntry = propList.GetPropertyItem("description", ADSTYPE_UNKNOWN)
 
' Clear all the values of the property entry.
For Each v In propEntry.Values
    Set propVal = v
    propVal.Clear
Next

propList.SetInfo

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If

    Set propList = Nothing
    Set propEntry = Nothing
    Set propVal = Nothing</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to use <b>IADsPropertyValue::Clear</b> to clear the value of the "description" property from a property list.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;activeds.h&gt;
#include &lt;stdio.h&gt;
 
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;
IADsPropertyValue *pVal = NULL;
IADs *pObj = NULL;
VARIANT var, varItem;
BSTR valStr;
IEnumVARIANT *pEnum = NULL;
LONG lstart, lend;
 
VariantInit(&amp;var);
VariantInit(&amp;varItem);
 
// Bind to the directory object.
HRESULT hr = ADsGetObject(L"LDAP://dc01/DC=Fabrikam,DC=com",
                          IID_IADsPropertyList,
                          (void**)&amp;pList);
if(FAILED(hr)){goto Cleanup;}

 
// Initialize the property cache.
hr = pList-&gt;QueryInterface(IID_IADs,(void**)&amp;pObj);
if(FAILED(hr)){goto Cleanup;}

pObj-&gt;GetInfo();
pObj-&gt;Release();
 
// Get a property entry.
hr = pList-&gt;GetPropertyItem(CComBSTR("description"), ADSTYPE_UNKNOWN, &amp;var);
if(FAILED(hr)){goto Cleanup;}

pList-&gt;Release();
hr = V_DISPATCH(&amp;var)-&gt;QueryInterface(IID_IADsPropertyEntry,
                                      (void**)&amp;pEntry);
if(FAILED(hr)){goto Cleanup;}
VariantClear(&amp;var);
 
// Get the value array of the property entry.
hr = pEntry-&gt;get_Values(&amp;var);
if(FAILED(hr)){goto Cleanup;}
SAFEARRAY *sa = V_ARRAY( &amp;var );
 
// Get the lower and upper bound, iterate, and print the values.
hr = SafeArrayGetLBound( sa, 1, &amp;lstart );
hr = SafeArrayGetUBound( sa, 1, &amp;lend );
printf(" Property value(s) = ");
for ( long idx=lstart; idx &lt; lend+1; idx++ )    {
    hr = SafeArrayGetElement( sa, &amp;idx, &amp;varItem );
    hr = V_DISPATCH(&amp;varItem)-&gt;QueryInterface(IID_IADsPropertyValue,
                                              (void**)&amp;pVal);
    VariantClear(&amp;varItem);
    hr = pVal-&gt;Clear();
    if(FAILED(hr)){goto Cleanup;}
}

pList-&gt;SetInfo();

Cleanup:
    if(pList)
        pList-&gt;Release();

    if(pEntry)
        pEntry-&gt;Release();

    if(pVal)
        pVal-&gt;Release();

    if(pObj)
        pObj-&gt;Release();

    if(pEnum)
        pEnum-&gt;Release();

    if(valStr)
        SysFreeString(valStr);

    VariantClear(&amp;var);
    VariantClear(&amp;varItem);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb">IADsPropertyValue</a>



<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">IADsPropertyValue Property Methods</a>
 

 

