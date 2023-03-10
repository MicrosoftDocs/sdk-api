---
UID: NF:unknwn.IClassFactory.CreateInstance
title: IClassFactory::CreateInstance
description: Creates an uninitialized object.
helpviewer_keywords: ["CreateInstance","CreateInstance method [COM]","CreateInstance method [COM]","IClassFactory interface","IClassFactory interface [COM]","CreateInstance method","IClassFactory.CreateInstance","IClassFactory::CreateInstance","_com_iclassfactory_createinstance","com.iclassfactory_createinstance","unknwn/IClassFactory::CreateInstance"]
old-location: com\iclassfactory_createinstance.htm
tech.root: com
ms.assetid: 45d34150-9e0b-4a76-a784-c81434ec73b8
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [COM], CreateInstance method [COM],IClassFactory interface, IClassFactory interface [COM],CreateInstance method, IClassFactory.CreateInstance, IClassFactory::CreateInstance, _com_iclassfactory_createinstance, com.iclassfactory_createinstance, unknwn/IClassFactory::CreateInstance
req.header: unknwn.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Unknwn.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IClassFactory::CreateInstance
 - unknwn/IClassFactory::CreateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Unknwn.h
api_name:
 - IClassFactory.CreateInstance
---

## -description

Creates an uninitialized object.

## -parameters

### -param pUnkOuter [in]

If the object is being created as part of an aggregate, specify a pointer to the controlling <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface of the aggregate. Otherwise, this parameter must be <b>NULL</b>.

### -param riid [in]

A reference to the identifier of the interface to be used to communicate with the newly created object. If <i>pUnkOuter</i> is <b>NULL</b>, this parameter is generally the IID of the initializing interface; if <i>pUnkOuter</i> is non-<b>NULL</b>, <i>riid</i> must be IID_IUnknown.

### -param ppvObject [out]

The address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppvObject</i> contains the requested interface pointer. If the object does not support the interface specified in <i>riid</i>, the implementation must set *<i>ppvObject</i> to <b>NULL</b>.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, and E_UNEXPECTED, as well as the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The specified object was created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CLASS_E_NOAGGREGATION</b></dt>
</dl>
</td>
<td width="60%">
The <i>pUnkOuter</i> parameter was non-<b>NULL</b> and the object does not support aggregation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOINTERFACE</b></dt>
</dl>
</td>
<td width="60%">
The object that <i>ppvObject</i> points to does not support the interface identified by <i>riid</i>.

</td>
</tr>
</table>

## -remarks

A COM server's implementation of <b>CreateInstance</b> must return a reference to an object contained in an apartment that belongs to the server's DCOM resolver. It must not return a reference to an object that is contained in a remote apartment.

The <a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a> interface is always on a class object. The <b>CreateInstance</b> method creates an uninitialized object of the class identified with the specified CLSID. When an object is created in this way, the CLSID must be registered in the system registry with the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a> function.

The <i>pUnkOuter</i> parameter indicates whether the object is being created as part of an aggregate. Object definitions are not required to support aggregation - they must be specifically designed and implemented to support it.

The <i>riid</i> parameter specifies the IID (interface identifier) of the interface through which you will communicate with the new object. If <i>pUnkOuter</i> is non-<b>NULL</b> (indicating aggregation), the value of the riid parameter must be IID_IUnknown. If the object is not part of an aggregate, riid often specifies the interface though which the object will be initialized.

For OLE embeddings, the initialization interface is <a href="/windows/desktop/api/objidl/nn-objidl-ipersiststorage">IPersistStorage</a>, but in other situations, other interfaces are used. To initialize the object, there must be a subsequent call to an appropriate method in the initializing interface. Common initialization functions include <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-initnew">IPersistStorage::InitNew</a> (for new, blank embeddable components), <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststorage-load">IPersistStorage::Load</a> (for reloaded embeddable components), <a href="/windows/desktop/api/objidl/nf-objidl-ipersiststream-load">IPersistStream::Load</a>, (for objects stored in a stream object) or <a href="/windows/desktop/api/objidl/nf-objidl-ipersistfile-load">IPersistFile::Load</a> (for objects stored in a file).

In general, if an application supports only one class of objects, and the class object is registered for single use, only one object can be created. The application must not create other objects, and a request to do so should return an error from <b>IClassFactory::CreateInstance</b>. The same is true for applications that support multiple classes, each with a class object registered for single use; a call to <b>CreateInstance</b> for one class followed by a call to <b>CreateInstance</b> for any of the classes that should return an error.

To avoid returning an error, applications that support multiple classes with single-use class objects can revoke the registered class object of the first class by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a> when a request for instantiating a second is received. For example, suppose there are two classes, A and B. When <b>CreateInstance</b> is called for class A, revoke the class object for B. When B is created, revoke the class object for A. This solution complicates shutdown because one of the class objects might have already been revoked (and cannot be revoked twice).

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a>

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a>

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject">CoRegisterClassObject</a>

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-corevokeclassobject">CoRevokeClassObject</a>

<a href="/windows/desktop/api/unknwnbase/nn-unknwnbase-iclassfactory">IClassFactory</a>