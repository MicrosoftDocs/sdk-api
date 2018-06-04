---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IADsPropertyList::ResetPropertyItem


## -description


The <b>IADsPropertyList::ResetPropertyItem</b> method removes the specified item from the list; that is, from the cache. You can specify the item to be removed by name (as a string) or by index (as an integer).


## -parameters




### -param varEntry






#### - VarData [in]

Entry to be reset.


## -returns



This method supports the standard <b>HRESULT</b> return values, including <b>S_OK</b>. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



<b>ResetPropertyItem</b> only affects the contents of the cache and does not affect the properties on the actual object in the directory; that is calling  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">SetInfo</a> after calling <b>ResetPropertyItem</b> does not delete the properties on the directory object.


#### Examples

The following code example shows how to implement <b>ResetPropertyItem</b>.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Dim propList As IADsPropertyList

On Error GoTo Cleanup
 
Set propList = GetObject("LDAP://DC=Fabrikam,DC=com")
 
'--- Now modify the cache using PutPropertyItem
Set propVal = New PropertyValue
'--- Property Value-----
propVal.CaseIgnoreString = "Fabrikam"
propVal.ADsType = ADSTYPE_CASE_IGNORE_STRING
 
'--- Property Entry ----
Set propEntry = New PropertyEntry
propEntry.Name = "adminDescription"
propEntry.Values = Array(propVal)
propEntry.ControlCode = ADS_PROPERTY_UPDATE
propEntry.ADsType = ADS_CASE_IGNORE_STRING
 
' --- Property List----
propList.PutPropertyItem (propEntry)
 
' Commit to the directory. Without this, the changes take place only in the cache.
propList.SetInfo 
 
propList.GetInfo
Debug.Print " Number of Properties = " &amp; propList.PropertyCount
propList.ResetPropertyItem "adminDescription"
 
' the property count should have been reduced by one.
Debug.Print "Number of properties = " &amp; propList.PropertyCount

Cleanup:
    If (Err.Number&lt;&gt;0) Then
        MsgBox("An error has occurred. " &amp; Err.Number)
    End If
    Set propList = Nothing
    Set propVal = Nothing
    Set propEntry = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example shows the effect produced by a call to <b>IADsPropertyList::ResetPropertyItem</b>. For more information and the listing of the <b>GetPropertyCache</b> function, see  <a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>. For more information and the listing of the <b>GetNextEntry</b> and <b>PropertyItem</b> functions, see  <a href="https://msdn.microsoft.com/2a12ba88-363b-41e3-bd05-8a71f5317097">IADsPropertyList::Next</a> and  <a href="https://msdn.microsoft.com/6e103872-ea2e-4178-9c8a-b958ae3bcf85">IADsPropertyList::Item</a> respectively.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IADsPropertyList *GetPropertyCache(LPWSTR);
IADsPropertyEntry *GetNextEntry(IADsPropertyList *);
IADsPropertyEntry *PropertyItem(IADsPropertyList *,LPWSTR);
 
void ResetItem(IADsPropertyList *pList, LPWSTR item)
{
    VARIANT var;
    VariantInit(&amp;var);

    if(!pList)
    {
        item = NULL;
        return;
    }

    V_BSTR(&amp;var)=SysAllocString(item);
    V_VT(&amp;var)=VT_BSTR;
 
    pList-&gt;ResetPropertyItem(var);
    VariantClear(&amp;var);
}
 
void TestResetItem()
{
    IADsPropertyEntry *pEntry = NULL;
    IADsPropertyList *pList = NULL;
    long count;
    BSTR bstr;
    HRESULT hr;
 
    pList = GetPropertyCache(L"WinNT://myComputer,computer");
 
    hr = pList-&gt;get_PropertyCount(&amp;count);
    if(SUCCEEDED(hr))
    {
        printf(" Count before item reset : %d\n",count);
    }
 
    printf("Walking up the property list before item reset: \n");
    for (int i=0; i&lt;count; i++)
    {
        pEntry = GetNextEntry(pList);
        hr = pEntry-&gt;get_Name(&amp;bstr);
        if(SUCCEEDED(hr))
        {
            printf("   Name : %S\n",bstr);
            SysFreeString(bstr);
        }
    }
 
    pList-&gt;Reset();   // Move the cursor to the beginning of the list.
 
    ResetItem(pList, L"Owner");
 
    hr = pList-&gt;get_PropertyCount(&amp;count);
    if(SUCCEEDED(hr))
    {
        printf(" Count after item reset : %d\n",count);
    }
 
    printf("Walking up the property list after item reset: \n");
 
    for (i=0; i&lt;count; i++)
    {
        pEntry = GetNextEntry(pList);
        hr = pEntry-&gt;get_Name(&amp;bstr);
        if(SUCCEEDED(hr))
        {
            printf("   Name : %S\n",bstr);
            SysFreeString(bstr);
        }
    }
 
    pEntry-&gt;Release();
    pList-&gt;Release();
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/3564b61a-5950-4d00-8ea1-86fecd5c6c4e">IADsPropertyList Property Methods</a>



<a href="https://msdn.microsoft.com/6e103872-ea2e-4178-9c8a-b958ae3bcf85">IADsPropertyList::Item</a>



<a href="https://msdn.microsoft.com/2a12ba88-363b-41e3-bd05-8a71f5317097">IADsPropertyList::Next</a>
 

 

