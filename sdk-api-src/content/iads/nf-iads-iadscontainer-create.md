---
UID: NF:iads.IADsContainer.Create
title: IADsContainer::Create (iads.h)
description: Sets up a request to create a directory object of the specified schema class and a given name in the container.
helpviewer_keywords: ["Create","Create method [ADSI]","Create method [ADSI]","IADsContainer interface","IADsContainer interface [ADSI]","Create method","IADsContainer.Create","IADsContainer::Create","_ds_iadscontainer_create","adsi.iadscontainer__create","adsi.iadscontainer_create","iads/IADsContainer::Create"]
old-location: adsi\iadscontainer_create.htm
tech.root: adsi
ms.assetid: 9498ef4d-7a03-487f-91a7-189f17a38a24
ms.date: 12/05/2018
ms.keywords: Create, Create method [ADSI], Create method [ADSI],IADsContainer interface, IADsContainer interface [ADSI],Create method, IADsContainer.Create, IADsContainer::Create, _ds_iadscontainer_create, adsi.iadscontainer__create, adsi.iadscontainer_create, iads/IADsContainer::Create
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
 - IADsContainer::Create
 - iads/IADsContainer::Create
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
 - IADsContainer.Create
---

# IADsContainer::Create


## -description

The <b>IADsContainer::Create</b> method sets up a request to create a directory object of the specified schema class and a given name in the container. The object is not made persistent until  <a href="/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> is called on the new object. This allows for setting mandatory properties on the new object.

## -parameters

### -param ClassName [in]

Name of the schema class object to be created. The name is that returned from the  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs::get_Schema</a> property method.

### -param RelativeName [in]

Relative name of the object as it is known in the underlying directory and identical to the one retrieved through the  <a href="/windows/desktop/api/iads/nn-iads-iads">IADs::get_Name</a> property method.

### -param ppObject [out]

Indirect pointer to the  <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface on the newly created object.

## -returns

This method supports the standard return values, including S_OK for a successful operation. For more information about error codes, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/iads/nf-iads-iadscontainer-delete">IADsContainer::Delete</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>