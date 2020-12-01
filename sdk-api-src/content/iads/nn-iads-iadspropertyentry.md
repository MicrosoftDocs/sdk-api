---
UID: NN:iads.IADsPropertyEntry
title: IADsPropertyEntry (iads.h)
description: The IADsPropertyEntry interface is used to manage a property entry in the property cache.
helpviewer_keywords: ["IADsPropertyEntry","IADsPropertyEntry interface [ADSI]","IADsPropertyEntry interface [ADSI]","described","PropertyEntry","_ds_iadspropertyentry","adsi.iadspropertyentry","iads/IADsPropertyEntry"]
old-location: adsi\iadspropertyentry.htm
tech.root: adsi
ms.assetid: 6c398d05-ac12-4c9a-b61a-70cd795c991f
ms.date: 12/05/2018
ms.keywords: IADsPropertyEntry, IADsPropertyEntry interface [ADSI], IADsPropertyEntry interface [ADSI],described, PropertyEntry, _ds_iadspropertyentry, adsi.iadspropertyentry, iads/IADsPropertyEntry
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
 - IADsPropertyEntry
 - iads/IADsPropertyEntry
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
 - IADsPropertyEntry
 - PropertyEntry
---

# IADsPropertyEntry interface


## -description

The <b>IADsPropertyEntry</b> interface is used to manage a property entry in the 
property cache. A property entry holds a value (or values) of an attribute as defined in the schema. It is identified by the name of the corresponding attribute. A property entry object allows a user to specify how its values are to be manipulated. Examples of such operations include "update,"
    "modify," and "delete".

Multiple property entries are managed by a property list. To access a property entry, you call  <a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-item">Item</a> or  <a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-getpropertyitem">GetPropertyItem</a> method on the  <a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a> interface.

Use the property methods of <b>IADsPropertyEntry</b> to examine and manipulate individual properties. Before calling the methods of this interface, you must call  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a> or  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a> explicitly to load the assigned property values of the object into the cache. After calling the methods of this interfaces, you must call  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> to save the changes in the persistent store of the underlying directory.

## -see-also

<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="/windows/desktop/ADSI/iadspropertyentry-property-methods">IADsPropertyEntry
    Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadspropertylist">IADsPropertyList</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-getpropertyitem">IADsPropertyList::GetPropertyItem</a>



<a href="/windows/desktop/api/iads/nf-iads-iadspropertylist-item">IADsPropertyList::Item</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>