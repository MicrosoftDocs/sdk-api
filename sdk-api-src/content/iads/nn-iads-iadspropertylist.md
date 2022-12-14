---
UID: NN:iads.IADsPropertyList
title: IADsPropertyList (iads.h)
description: The IADsPropertyList interface is used to modify, read, and update a list of property entries in the property cache of an object.
helpviewer_keywords: ["IADsPropertyList","IADsPropertyList interface [ADSI]","IADsPropertyList interface [ADSI]","described","_ds_iadspropertylist","adsi.iadspropertylist","iads/IADsPropertyList"]
old-location: adsi\iadspropertylist.htm
tech.root: adsi
ms.assetid: 70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2
ms.date: 12/05/2018
ms.keywords: IADsPropertyList, IADsPropertyList interface [ADSI], IADsPropertyList interface [ADSI],described, _ds_iadspropertylist, adsi.iadspropertylist, iads/IADsPropertyList
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
 - IADsPropertyList
 - iads/IADsPropertyList
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
 - IADsPropertyList
---

# IADsPropertyList interface


## -description

The <b>IADsPropertyList</b> interface is used to modify, read, and update a list of property entries in the property cache of an object. It serves to enumerate, modify, and purge the contained property entries. Use the enumeration method of this interface to identify initialized properties. This is different from using the schema to determine all possible attributes that an ADSI object can have and which properties have been set.
   

Call the methods of the <b>IADsPropertyList</b> interface to examine and manipulate the property list on the client. Before calling the methods of this interface, you must call  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a> or  <a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a> explicitly to load the assigned property values of the object into the cache. After calling the methods of this interface, you must call  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> to save the changes in the persistent store of the underlying directory.

To obtain the property list of an ADSI object, bind to its <b>IADsPropertyList</b> interface. You must call the <a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">GetInfo</a> method before calling other methods of property list object, if the property cache has not been initialized.

## -inheritance

The <b>IADsPropertyList</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsPropertyList</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>



<a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="/windows/desktop/ADSI/iadspropertylist-property-methods">IADsPropertyList Property Methods</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
