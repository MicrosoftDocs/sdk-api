---
UID: NN:iads.IADsPropertyValue
title: IADsPropertyValue (iads.h)
description: Used to represent the value of an IADsPropertyEntry object in a predefined data type.
helpviewer_keywords: ["IADsPropertyValue","IADsPropertyValue interface [ADSI]","IADsPropertyValue interface [ADSI]","described","PropertyValue","_ds_iadspropertyvalue","adsi.iadspropertyvalue","iads/IADsPropertyValue"]
old-location: adsi\iadspropertyvalue.htm
tech.root: adsi
ms.assetid: 7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb
ms.date: 12/05/2018
ms.keywords: IADsPropertyValue, IADsPropertyValue interface [ADSI], IADsPropertyValue interface [ADSI],described, PropertyValue, _ds_iadspropertyvalue, adsi.iadspropertyvalue, iads/IADsPropertyValue
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
 - IADsPropertyValue
 - iads/IADsPropertyValue
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
 - IADsPropertyValue
 - PropertyValue
---

# IADsPropertyValue interface


## -description

The <b>IADsPropertyValue</b> interface is used to represent the value of an <a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> object in a predefined data type. This interface exposes several properties for obtaining data values in the corresponding data format.

The <a href="/windows/desktop/ADSI/iadspropertyentry-property-methods">IADsPropertyEntry.Values</a> property contains an array of <b>IADsPropertyValue</b> objects. Each of the <b>IADsPropertyValue</b> objects contains a single value of the <a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> object. For more information and a code example for creating entirely new property entries and values, see <a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-putpropertyitem">IADsPropertyList.PutPropertyItem</a>.

When obtaining values in a format not provided by one of the properties of this interface, use the  <a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a> interface.

Before calling the methods of this interfaces, call  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs.GetInfo</a> or  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs.GetInfoEx</a> explicitly to load the assigned values of the object into the cache, if the cache has not been initialized. After modifying the properties of this interface, call  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs.SetInfo</a> to save the changes to the persistent store of the underlying directory.

## -inheritance

The <b>IADsPropertyValue</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsPropertyValue</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a>



<a href="/windows/desktop/ADSI/iadspropertyvalue-property-methods">IADsPropertyValue Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
