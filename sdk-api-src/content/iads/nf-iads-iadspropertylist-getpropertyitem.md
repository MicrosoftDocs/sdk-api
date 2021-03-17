---
UID: NF:iads.IADsPropertyList.GetPropertyItem
title: IADsPropertyList::GetPropertyItem (iads.h)
description: Retrieves the item that matches the name from the list.
helpviewer_keywords: ["GetPropertyItem","GetPropertyItem method [ADSI]","GetPropertyItem method [ADSI]","IADsPropertyList interface","IADsPropertyList interface [ADSI]","GetPropertyItem method","IADsPropertyList.GetPropertyItem","IADsPropertyList::GetPropertyItem","_ds_iadspropertylist_getpropertyitem","adsi.iadspropertylist__getpropertyitem","adsi.iadspropertylist_getpropertyitem","iads/IADsPropertyList::GetPropertyItem"]
old-location: adsi\iadspropertylist_getpropertyitem.htm
tech.root: adsi
ms.assetid: 1de86caa-c14c-4dc0-bf56-5fa33279e30a
ms.date: 12/05/2018
ms.keywords: GetPropertyItem, GetPropertyItem method [ADSI], GetPropertyItem method [ADSI],IADsPropertyList interface, IADsPropertyList interface [ADSI],GetPropertyItem method, IADsPropertyList.GetPropertyItem, IADsPropertyList::GetPropertyItem, _ds_iadspropertylist_getpropertyitem, adsi.iadspropertylist__getpropertyitem, adsi.iadspropertylist_getpropertyitem, iads/IADsPropertyList::GetPropertyItem
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
 - IADsPropertyList::GetPropertyItem
 - iads/IADsPropertyList::GetPropertyItem
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
 - IADsPropertyList.GetPropertyItem
---

# IADsPropertyList::GetPropertyItem


## -description

The <b>IADsPropertyList::GetPropertyItem</b> method retrieves the item that matches the name from the list.

## -parameters

### -param bstrName [in]

Contains the name of the requested property.

### -param lnADsType [in]

Contains one of the <a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a> enumeration values that determines the data type to be used in interpreting the requested property. If the type is unknown, this parameter can be set to <b>ADSTYPE_UNKNOWN</b>. For schemaless servers, the user must specify the type.

### -param pVariant [in, out]

Address of a caller-allocated <b>VARIANT</b> variable. On return, the <b>VARIANT</b> contains the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer of the object which implements the  <a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> interface for the retrieved attribute.

Any memory allocated for this parameter must be released with the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> function when the data is no longer required.

## -returns

This method supports the standard <b>HRESULT</b> return values, including <b>S_OK</b>. If the requested property item is not found, the method returns <b>ADS_PROPERTY_NOT_FOUND</b>. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

The property of the <a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue">IADsPropertyValue</a> object returned by this method that can be used will depend on the type specified in <i>lnADsType</i>. The following table maps the data type to the appropriate <a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> property.

<table>
<tr>
<th><i>lnADsType</i> value</th>
<th>
<a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue">IADsPropertyValue</a> property to use</th>
</tr>
<tr>
<td><b>ADSTYPE_INVALID</b></td>
<td>Not available.</td>
</tr>
<tr>
<td><b>ADSTYPE_DN_STRING</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">DNString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_CASE_EXACT_STRING</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">CaseExactString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_CASE_IGNORE_STRING</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">CaseIgnoreString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_PRINTABLE_STRING</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">PrintableString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_NUMERIC_STRING</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">NumericString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_BOOLEAN</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">Boolean</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_INTEGER</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">Integer</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_OCTET_STRING</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">OctetString</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_UTC_TIME</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">UTCTime</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_LARGE_INTEGER</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">LargeInteger</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_PROV_SPECIFIC</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (VT_ARRAY | VT_UI1).</td>
</tr>
<tr>
<td><b>ADSTYPE_OBJECT_CLASS</b></td>
<td>Not available.</td>
</tr>
<tr>
<td><b>ADSTYPE_CASEIGNORE_LIST</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsCaseIgnoreList).</td>
</tr>
<tr>
<td><b>ADSTYPE_OCTET_LIST</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsOctetList).</td>
</tr>
<tr>
<td><b>ADSTYPE_PATH</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsPath).</td>
</tr>
<tr>
<td><b>ADSTYPE_POSTALADDRESS</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsPostalAddress).</td>
</tr>
<tr>
<td><b>ADSTYPE_TIMESTAMP</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsTimestamp).</td>
</tr>
<tr>
<td><b>ADSTYPE_BACKLINK</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsBackLink).</td>
</tr>
<tr>
<td><b>ADSTYPE_TYPEDNAME</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsTypedName).</td>
</tr>
<tr>
<td><b>ADSTYPE_HOLD</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsHold).</td>
</tr>
<tr>
<td><b>ADSTYPE_NETADDRESS</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsNetAddress).</td>
</tr>
<tr>
<td><b>ADSTYPE_REPLICAPOINTER</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsReplicaPointer).</td>
</tr>
<tr>
<td><b>ADSTYPE_FAXNUMBER</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsFaxNumber).</td>
</tr>
<tr>
<td><b>ADSTYPE_EMAIL</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsEmail).</td>
</tr>
<tr>
<td><b>ADSTYPE_NT_SECURITY_DESCRIPTOR</b></td>
<td>
<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">SecurityDescriptor</a>
</td>
</tr>
<tr>
<td><b>ADSTYPE_UNKNOWN</b></td>
<td>Not available.</td>
</tr>
<tr>
<td><b>ADSTYPE_DN_WITH_BINARY</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsDNWithBinary).</td>
</tr>
<tr>
<td><b>ADSTYPE_DN_WITH_STRING</b></td>
<td>Use <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">IADsPropertyValue2::GetObjectProperty</a> (IADsDNWithString).</td>
</tr>
</table>
 


#### Examples

The following  code example shows how to retrieve a property entry using the <b>GetPropertyItem</b> method.


```vb
Const ADSTYPE_CASE_IGNORE_STRING = 3
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

```


The following code example shows how to retrieve a property entry using the <b>GetPropertyItem</b> method. It assumes that the <a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a> interface has been properly retrieved. For more information about how to load the property cache, see the <a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">GetPropertyCache</a> example function  in  <b>IADsPropertyList</b>.


```cpp
#include <activeds.h>
#include <stdio.h>
 
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
   VariantInit(&var);

   if(!pList || !entryName)
   {
      _tprintf("Invalid argument...");
      return NULL;
   }
 
   // Get a property entry.
   hr = pList->GetPropertyItem(entryName, entryType, &var);
   hr = V_DISPATCH(&var)->QueryInterface(IID_IADsPropertyEntry,
                                         (void**)&pEntry);
   VariantClear(&var);
 
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
    HRESULT hr = pEntry->get_Name(&nm);
    if(SUCCEEDED(hr))
    {
        printf("Property name = %S\n",nm);
        SysFreeString(nm);
    }
}
 
if(pList)
    pList->Release();
if(pEntry)
    pEntry->Release();
```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/win32/api/iads/ne-iads-adstypeenum">ADSTYPEENUM</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>



<a href="/windows/desktop/ADSI/iadspropertylist-property-methods">IADsPropertyList Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a>