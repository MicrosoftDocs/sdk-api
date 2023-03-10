---
UID: NF:iads.IDirectoryObject.DeleteDSObject
title: IDirectoryObject::DeleteDSObject (iads.h)
description: Deletes a leaf object in a directory tree.
helpviewer_keywords: ["DeleteDSObject","DeleteDSObject method [ADSI]","DeleteDSObject method [ADSI]","IDirectoryObject interface","IDirectoryObject interface [ADSI]","DeleteDSObject method","IDirectoryObject.DeleteDSObject","IDirectoryObject::DeleteDSObject","_ds_idirectoryobject_deletedsobject","adsi.idirectoryobject__deletedsobject","adsi.idirectoryobject_deletedsobject","iads/IDirectoryObject::DeleteDSObject"]
old-location: adsi\idirectoryobject_deletedsobject.htm
tech.root: adsi
ms.assetid: bb7bed74-1420-4b46-92a9-ebe31f2d88fd
ms.date: 12/05/2018
ms.keywords: DeleteDSObject, DeleteDSObject method [ADSI], DeleteDSObject method [ADSI],IDirectoryObject interface, IDirectoryObject interface [ADSI],DeleteDSObject method, IDirectoryObject.DeleteDSObject, IDirectoryObject::DeleteDSObject, _ds_idirectoryobject_deletedsobject, adsi.idirectoryobject__deletedsobject, adsi.idirectoryobject_deletedsobject, iads/IDirectoryObject::DeleteDSObject
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
 - IDirectoryObject::DeleteDSObject
 - iads/IDirectoryObject::DeleteDSObject
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
 - IDirectoryObject.DeleteDSObject
---

# IDirectoryObject::DeleteDSObject


## -description

The <b>IDirectoryObject::DeleteDSObject</b> method deletes a leaf object in a directory tree.

## -parameters

### -param pszRDNName

The relative distinguished name (relative path) of the object to be deleted.

## -returns

This method returns the standard return values, including S_OK for a successful operation. For more information and other return values, see  <a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>.

## -remarks

To delete a container object and its children, use the  <a href="/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject">IADsDeleteOps::DeleteObject</a> method.


#### Examples

The following C/C++ code example shows how to delete a user object.


```cpp
HRESULT hr;
IDirectoryObject *pDirObject=NULL;
hr = ADsGetObject(L"LDAP://OU=Sales,DC=Fabrikam,DC=com",
    IID_IDirectoryObject, (void**) &pDirObject );
 
if ( SUCCEEDED(hr) )
{
    hr = pDirObject->DeleteDSObject( L"CN=Jeff Smith" );

    pDirObject->Release();
} 

```

## -see-also

<a href="/windows/desktop/ADSI/adsi-error-codes">ADSI Error Codes</a>



<a href="/windows/desktop/api/iads/nf-iads-iadsdeleteops-deleteobject">IADsDeleteOps::DeleteObject</a>



<a href="/windows/desktop/api/iads/nn-iads-idirectoryobject">IDirectoryObject</a>