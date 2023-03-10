---
UID: NF:iads.IADsCollection.Add
title: IADsCollection::Add (iads.h)
description: Adds a named item to the collection.
helpviewer_keywords: ["Add","Add method [ADSI]","Add method [ADSI]","IADsCollection interface","IADsCollection interface [ADSI]","Add method","IADsCollection.Add","IADsCollection::Add","_ds_iadscollection_add","adsi.iadscollection__add","adsi.iadscollection_add","iads/IADsCollection::Add"]
old-location: adsi\iadscollection_add.htm
tech.root: adsi
ms.assetid: c4f0dc3e-238c-4fd3-adb7-9d467efc8c3d
ms.date: 12/05/2018
ms.keywords: Add, Add method [ADSI], Add method [ADSI],IADsCollection interface, IADsCollection interface [ADSI],Add method, IADsCollection.Add, IADsCollection::Add, _ds_iadscollection_add, adsi.iadscollection__add, adsi.iadscollection_add, iads/IADsCollection::Add
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
 - IADsCollection::Add
 - iads/IADsCollection::Add
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
 - IADsCollection.Add
---

# IADsCollection::Add


## -description

The <b>IADsCollection::Add</b> method adds a named item to the collection.

## -parameters

### -param bstrName [in]

The <b>BSTR</b> value that specifies the item name.  <a href="/windows/desktop/api/iads/nf-iads-iadscollection-getobject">IADsCollection::GetObject</a> and  <a href="/windows/desktop/api/iads/nf-iads-iadscollection-remove">IADsCollection::Remove</a> reference the item by this name.

### -param vItem [in]

Item value. When the item is an object, this parameter holds the  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface pointer on the object.

## -returns

This method supports the standard return values, as well as the following.
      

For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

Collections for a directory service can also consist of a set of immutable objects.

This method is not supported in any of the  <a href="/windows/desktop/ADSI/adsi-system-providers">ADSI system providers</a>.

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/ADSI/adsi-system-providers">ADSI System
  Providers</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscollection">IADsCollection</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscollection-getobject">IADsCollection::GetObject</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscollection-remove">IADsCollection::Remove</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>