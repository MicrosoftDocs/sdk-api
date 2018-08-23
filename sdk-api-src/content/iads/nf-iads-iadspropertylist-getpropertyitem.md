---
UID: NF:iads.IADsPropertyList.GetPropertyItem
title: IADsPropertyList::GetPropertyItem
author: windows-sdk-content
description: Retrieves the item that matches the name from the list.
old-location: adsi\iadspropertylist_getpropertyitem.htm
old-project: ADSI
ms.assetid: 1de86caa-c14c-4dc0-bf56-5fa33279e30a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetPropertyItem, GetPropertyItem method [ADSI], GetPropertyItem method [ADSI],IADsPropertyList interface, IADsPropertyList interface [ADSI],GetPropertyItem method, IADsPropertyList.GetPropertyItem, IADsPropertyList::GetPropertyItem, _ds_iadspropertylist_getpropertyitem, adsi.iadspropertylist__getpropertyitem, adsi.iadspropertylist_getpropertyitem, iads/IADsPropertyList::GetPropertyItem
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
 - IADsPropertyList.GetPropertyItem
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsPropertyList::GetPropertyItem


## -description


The <b>IADsPropertyList::GetPropertyItem</b> method retrieves the item that matches the name from the list.


## -parameters




### -param bstrName [in]

Contains the name of the requested property.


### -param lnADsType [in]

Contains one of the <a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a> enumeration values that determines the data type to be used in interpreting the requested property. If the type is unknown, this parameter can be set to <b>ADSTYPE_UNKNOWN</b>. For schemaless servers, the user must specify the type.


### -param pVariant [in, out]

Address of a caller-allocated <b>VARIANT</b> variable. On return, the <b>VARIANT</b> contains the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface pointer of the object which implements the  <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> interface for the retrieved attribute.

Any memory allocated for this parameter must be released with the <a href="https://msdn.microsoft.com/en-us/library/ms221165(v=VS.85).aspx">VariantClear</a> function when the data is no longer required.


## -returns



This method supports the standard <b>HRESULT</b> return values, including <b>S_OK</b>. If the requested property item is not found, the method returns <b>ADS_PROPERTY_NOT_FOUND</b>. For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -remarks



The property of the <a href="https://msdn.microsoft.com/7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb">IADsPropertyValue</a> object returned by this method that can be used will depend on the type specified in <i>lnADsType</i>. The following table maps the data type to the appropriate <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> property.

<table>
<tr>
<th><i>lnADsType</i> value</th>
<th>
<a href="https://msdn.microsoft.com/7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb">IADsPropertyValue</a> property to use</th>
</tr>
<tr>
<td><b>ADSTYPE_INVALID</b></td>
<td>Not available.</td>
</tr>
<tr>
<td><b>ADSTYPE_DN_STRING</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">DNString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_CASE_EXACT_STRING</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">CaseExactString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_CASE_IGNORE_STRING</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">CaseIgnoreString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_PRINTABLE_STRING</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">PrintableString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_NUMERIC_STRING</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">NumericString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">Boolean</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_INTEGER</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">Integer</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_OCTET_STRING</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">OctetString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_UTC_TIME</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">UTCTime</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_LARGE_INTEGER</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">LargeInteger</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_PROV_SPECIFIC</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (VT_ARRAY | VT_UI1).</td>
</tr>
<tr>
<td><b>ADSTYPE_OBJECT_CLASS</b></td>
<td>Not available.</td>
</tr>
<tr>
<td><b>ADSTYPE_CASEIGNORE_LIST</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsCaseIgnoreList).</td>
</tr>
<tr>
<td><b>ADSTYPE_OCTET_LIST</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsOctetList).</td>
</tr>
<tr>
<td><b>ADSTYPE_PATH</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsPath).</td>
</tr>
<tr>
<td><b>ADSTYPE_POSTALADDRESS</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsPostalAddress).</td>
</tr>
<tr>
<td><b>ADSTYPE_TIMESTAMP</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsTimestamp).</td>
</tr>
<tr>
<td><b>ADSTYPE_BACKLINK</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsBackLink).</td>
</tr>
<tr>
<td><b>ADSTYPE_TYPEDNAME</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsTypedName).</td>
</tr>
<tr>
<td><b>ADSTYPE_HOLD</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsHold).</td>
</tr>
<tr>
<td><b>ADSTYPE_NETADDRESS</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsNetAddress).</td>
</tr>
<tr>
<td><b>ADSTYPE_REPLICAPOINTER</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsReplicaPointer).</td>
</tr>
<tr>
<td><b>ADSTYPE_FAXNUMBER</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsFaxNumber).</td>
</tr>
<tr>
<td><b>ADSTYPE_EMAIL</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsEmail).</td>
</tr>
<tr>
<td><b>ADSTYPE_NT_SECURITY_DESCRIPTOR</b></td>
<td>
<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">SecurityDescriptor</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_UNKNOWN</b></td>
<td>Not available.</td>
</tr>
<tr>
<td><b>ADSTYPE_DN_WITH_BINARY</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsDNWithBinary).</td>
</tr>
<tr>
<td><b>ADSTYPE_DN_WITH_STRING</b></td>
<td>Use <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">IADsPropertyValue2::GetObjectProperty</a> (IADsDNWithString).</td>
</tr>
</table>
 


#### Examples

The following  code example shows how to retrieve a property entry using the <b>GetPropertyItem</b> method.

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>Const ADSTYPE_CASE_IGNORE_STRING = 3
Dim propList As IADsPropertyList
Dim propEntry As IADsPropertyEntry
Dim propVal As IADsPropertyValue

Set propList = GetObject("LDAP://dc01/DC=Fabrikam,DC=com")
propList.GetInfo
 
Set propEntry = propList.GetPropertyItem("dc", ADSTYPE_CASE_IGNORE_STRING)
 
For Each v In propEntry.Values
    Set propVal = v

    ' Use the CaseIgnoreString property because the ADSTYPE_CASE_IGNORE_STRING 
    ' type was requested in GetPropertyItem.
    Debug.Print propVal.CaseIgnoreString
Next

Set propList = Nothing
Set propEntry = Nothing
Set propVal = Nothing
</pre>
</td>
</tr>
</table></span></div>
The following code example shows how to retrieve a property entry using the <b>GetPropertyItem</b> method. It assumes that the <a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a> interface has been properly retrieved. For more information about how to load the property cache, see the <a href="https://msdn.microsoft.com/en-us/library/Aa706102(v=VS.85).aspx">GetPropertyCache</a> example function  in  <b>IADsPropertyList</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;activeds.h&gt;
#include &lt;stdio.h&gt;
 
/////////////////////////////////////////////////////////
// Function to retrieve a specified property entry 
// using the IADsPropertyList::GetPropertyItem method.
/////////////////////////////////////////////////////////
IADsPropertyEntry *GetPropertyItem(
      IADsPropertyList *pList, 
      BSTR entryName,
      long entryType)
{
   IADsPropertyEntry *pEntry;
   VARIANT var;
   VariantInit(&amp;var);

   if(!pList || !entryName)
   {
      _tprintf("Invalid argument...");
      return NULL;
   }
 
   // Get a property entry.
   hr = pList-&gt;GetPropertyItem(entryName, entryType, &amp;var);
   hr = V_DISPATCH(&amp;var)-&gt;QueryInterface(IID_IADsPropertyEntry,
                                         (void**)&amp;pEntry);
   VariantClear(&amp;var);
 
   return pEntry;
}
 
///////////////////////////////////////////////////////
// Examine a property entry.
///////////////////////////////////////////////////////
IADsPropertyList *pList = NULL;
IADsPropertyEntry *pEntry = NULL;

pList = GetPropertyCache(L"LDAP://dc01/DC=Fabrikam,DC=COM");
 
if(pList)
{
    pEntry = GetPropertyItem(pList, L"dc", ADSTYPE_CASE_IGNORE_STRING);
}

if(pEntry)
{ 
    BSTR nm;
    HRESULT hr = pEntry-&gt;get_Name(&amp;nm);
    if(SUCCEEDED(hr))
    {
        printf("Property name = %S\n",nm);
        SysFreeString(nm);
    }
}
 
if(pList)
    pList-&gt;Release();
if(pEntry)
    pEntry-&gt;Release();</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/e601bae5-80bf-43f5-846f-11327889419a">ADSTYPEENUM</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/3564b61a-5950-4d00-8ea1-86fecd5c6c4e">IADsPropertyList Property Methods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221165(v=VS.85).aspx">VariantClear</a>
 

 

