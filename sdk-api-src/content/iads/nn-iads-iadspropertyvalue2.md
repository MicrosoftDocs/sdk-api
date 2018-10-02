---
UID: NN:iads.IADsPropertyValue2
title: IADsPropertyValue2
author: windows-sdk-content
description: Used to represent the value of an IADsPropertyEntry object in any data format.
old-location: adsi\iadspropertyvalue2.htm
tech.root: ADSI
ms.assetid: 57a3b413-f658-4793-abad-358455b5b9f4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IADsPropertyValue2, IADsPropertyValue2 interface [ADSI], IADsPropertyValue2 interface [ADSI],described, _ds_iadspropertyvalue2, adsi.iadspropertyvalue2, iads/IADsPropertyValue2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IADsPropertyValue2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsPropertyValue2 interface


## -description


The <b>IADsPropertyValue2</b> interface is 
    used to represent the value of an 
    <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> object in any data format, 
    including new or customer-defined data types. This interface is also useful for handling attribute values for 
    multiple directory services.

The <a href="https://msdn.microsoft.com/73b0f6d4-55db-46cf-a781-e10bc4fcf2db">IADsPropertyEntry.Values</a> 
    property contains an array of <b>IADsPropertyValue2</b> 
    objects. Each of the <a href="https://msdn.microsoft.com/7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb">IADsPropertyValue</a> objects contains 
    a single value of the <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> object. For 
    more information and  a code example for creating entirely new property entries and values, see 
    <a href="https://msdn.microsoft.com/16af5cbf-3b87-467e-8e72-0110bcf95295">IADsPropertyList.PutPropertyItem</a>.

Before calling the methods of this interfaces, you must call 
    <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs.GetInfo</a> or 
    <a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs.GetInfoEx</a> explicitly to load the assigned values of 
    the object into the cache, if the cache has not been initialized. After modifying the values of the object, you 
    must call <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs.SetInfo</a> to save the changes to the 
    persistent store of the underlying directory.

This interface is more versatile than the 
    <a href="https://msdn.microsoft.com/7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb">IADsPropertyValue</a> because this interface can be used to 
    obtain any data type. The <b>IADsPropertyValue</b> interface 
    can only be used to obtain a limited number of data types.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPropertyValue2</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsPropertyValue2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IADsPropertyValue2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">GetObjectProperty</a>
</td>
<td align="left" width="63%">
Retrieves the value of an attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53dad13f-7df7-4c1d-8c8a-946c291b20c6">PutObjectProperty</a>
</td>
<td align="left" width="63%">
Sets the value of an attribute.

</td>
</tr>
</table> 


## -remarks



The following table lists the <i>lnADsType</i> parameter values in the 
     <a href="https://msdn.microsoft.com/a189f106-23dc-441b-8d97-c03d4c49a4a1">GetObjectProperty</a> and 
     <a href="https://msdn.microsoft.com/53dad13f-7df7-4c1d-8c8a-946c291b20c6">PutObjectProperty</a> methods to the 
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
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/d49e3339-8488-44c1-9d60-706492e65abc">IADsLargeInteger</a>)

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
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/e587d603-d235-4449-986c-89f0fdb86ab6">IADsCaseIgnoreList</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_OCTET_LIST</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/66ec49d6-43c5-4fc8-a90d-5847fd2ffe50">IADsOctetList</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_PATH</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/e588195c-eb4f-48d3-a2fa-777dd6dc2901">IADsPath</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_POSTALADDRESS</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/53ff56a6-60ee-44a1-b18b-18f17efe2acd">IADsPostalAddress</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_TIMESTAMP</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/5f24e6e9-ad5b-4d5b-b3f3-cc3aca599bc1">IADsTimestamp</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_BACKLINK</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/2876e8c5-8cfa-4bcc-91ba-c2f71bfbe622">IADsBackLink</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_TYPEDNAME</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/ed57fad7-6cc6-4127-b8d2-da295bc0c5fe">IADsTypedName</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_HOLD</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/ccc22915-0f67-4089-9ddc-491b6f7ef554">IADsHold</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_NETADDRESS</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/71e48dd4-4e86-494f-835e-38bda29fc543">IADsNetAddress</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_REPLICAPOINTER</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/c34eab26-540e-4400-873e-7af09fda0bbf">IADsReplicaPointer</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_FAXNUMBER</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/1c78bb35-dfa9-40f0-b3a4-db4a1c212cf7">IADsFaxNumber</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_EMAIL</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/ce788365-9e43-4bce-89c3-07506cb308fa">IADsEmail</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_NT_SECURITY_DESCRIPTOR</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/c77547ab-e666-4d72-b8ef-4b2f3d61ad38">IADsSecurityDescriptor</a>)

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
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/dd64f0bd-1211-4e6f-93b5-87c079999208">IADsDNWithBinary</a>)

</td>
</tr>
<tr>
<td>
<b>ADSTYPE_DN_WITH_STRING</b>

</td>
<td>
<b>VT_DISPATCH</b> (<a href="https://msdn.microsoft.com/112985e7-6e96-42fb-a4cb-916296d4a524">IADsDNWithString</a>)

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a>



<a href="https://msdn.microsoft.com/70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2">IADsPropertyList</a>



<a href="https://msdn.microsoft.com/7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb">IADsPropertyValue</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

