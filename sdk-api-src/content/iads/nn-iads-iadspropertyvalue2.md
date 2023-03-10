---
UID: NN:iads.IADsPropertyValue2
title: IADsPropertyValue2 (iads.h)
description: Used to represent the value of an IADsPropertyEntry object in any data format.
helpviewer_keywords: ["IADsPropertyValue2","IADsPropertyValue2 interface [ADSI]","IADsPropertyValue2 interface [ADSI]","described","_ds_iadspropertyvalue2","adsi.iadspropertyvalue2","iads/IADsPropertyValue2"]
old-location: adsi\iadspropertyvalue2.htm
tech.root: adsi
ms.assetid: 57a3b413-f658-4793-abad-358455b5b9f4
ms.date: 12/05/2018
ms.keywords: IADsPropertyValue2, IADsPropertyValue2 interface [ADSI], IADsPropertyValue2 interface [ADSI],described, _ds_iadspropertyvalue2, adsi.iadspropertyvalue2, iads/IADsPropertyValue2
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
 - IADsPropertyValue2
 - iads/IADsPropertyValue2
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
 - IADsPropertyValue2
---

# IADsPropertyValue2 interface


## -description

The <b>IADsPropertyValue2</b> interface is 
    used to represent the value of an 
    <a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> object in any data format, 
    including new or customer-defined data types. This interface is also useful for handling attribute values for 
    multiple directory services.

The <a href="/windows/desktop/ADSI/iadspropertyentry-property-methods">IADsPropertyEntry.Values</a> 
    property contains an array of <b>IADsPropertyValue2</b> 
    objects. Each of the <a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue">IADsPropertyValue</a> objects contains 
    a single value of the <a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> object. For 
    more information and  a code example for creating entirely new property entries and values, see 
    <a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-putpropertyitem">IADsPropertyList.PutPropertyItem</a>.

Before calling the methods of this interfaces, you must call 
    <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs.GetInfo</a> or 
    <a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs.GetInfoEx</a> explicitly to load the assigned values of 
    the object into the cache, if the cache has not been initialized. After modifying the values of the object, you 
    must call <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs.SetInfo</a> to save the changes to the 
    persistent store of the underlying directory.

This interface is more versatile than the 
    <a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue">IADsPropertyValue</a> because this interface can be used to 
    obtain any data type. The <b>IADsPropertyValue</b> interface 
    can only be used to obtain a limited number of data types.

## -inheritance

The <b>IADsPropertyValue2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsPropertyValue2</b> also has these types of members:

## -remarks

The following table lists the <i>lnADsType</i> parameter values in the 
     <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-getobjectproperty">GetObjectProperty</a> and 
     <a href="/windows/desktop/api/iads/nf-iads-iadspropertyvalue2-putobjectproperty">PutObjectProperty</a> methods to the 
     corresponding <i>pvProp</i> data type.

<table>
<tr>
<th><i>lnADsType</i> value</th>
<th><i>pvProp</i> data type</th>
</tr>
<tr>
<td>
<b>ADSTYPE_INVALID</b>

</td>
<td>
Not available.

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_DN_STRING</b>

</td>
<td>
<b>VT_BSTR</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_CASE_EXACT_STRING</b>

</td>
<td>
<b>VT_BSTR</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_CASE_IGNORE_STRING</b>

</td>
<td>
<b>VT_BSTR</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_PRINTABLE_STRING</b>

</td>
<td>
<b>VT_BSTR</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_NUMERIC_STRING</b>

</td>
<td>
<b>VT_BSTR</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_BOOLEAN</b>

</td>
<td>
<b>VT_BOOL</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_INTEGER</b>

</td>
<td>
<b>VT_I4</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_OCTET_STRING</b>

</td>
<td>
<b>VT_ARRAY</b> | <b>VT_UI4</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_UTC_TIME</b>

</td>
<td>
<b>VT_DATE</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_LARGE_INTEGER</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadslargeinteger">IADsLargeInteger</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_PROV_SPECIFIC</b>

</td>
<td>
<b>VT_ARRAY</b> | <b>VT_UI1</b>

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_OBJECT_CLASS</b>

</td>
<td>
Not available.

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_CASEIGNORE_LIST</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadscaseignorelist">IADsCaseIgnoreList</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_OCTET_LIST</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadsoctetlist">IADsOctetList</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_PATH</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadspath">IADsPath</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_POSTALADDRESS</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadspostaladdress">IADsPostalAddress</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_TIMESTAMP</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadstimestamp">IADsTimestamp</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_BACKLINK</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadsbacklink">IADsBackLink</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_TYPEDNAME</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadstypedname">IADsTypedName</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_HOLD</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadshold">IADsHold</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_NETADDRESS</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadsnetaddress">IADsNetAddress</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_REPLICAPOINTER</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadsreplicapointer">IADsReplicaPointer</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_FAXNUMBER</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadsfaxnumber">IADsFaxNumber</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_EMAIL</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadsemail">IADsEmail</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_NT_SECURITY_DESCRIPTOR</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor">IADsSecurityDescriptor</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_UNKNOWN</b>

</td>
<td>
Not available.

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_DN_WITH_BINARY</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadsdnwithbinary">IADsDNWithBinary</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_DN_WITH_STRING</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="/windows/desktop/api/iads/nn-iads-iadsdnwithstring">IADsDNWithString</a>)

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue">IADsPropertyValue</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
