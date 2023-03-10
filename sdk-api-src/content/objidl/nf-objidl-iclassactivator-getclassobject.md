---
UID: NF:objidl.IClassActivator.GetClassObject
title: IClassActivator::GetClassObject (objidl.h)
description: Retrieves a class object.
helpviewer_keywords: ["GetClassObject","GetClassObject method [COM]","GetClassObject method [COM]","IClassActivator interface","IClassActivator interface [COM]","GetClassObject method","IClassActivator.GetClassObject","IClassActivator::GetClassObject","_com_iclassactivator_getclassobject","com.iclassactivator_getclassobject","objidl/IClassActivator::GetClassObject"]
old-location: com\iclassactivator_getclassobject.htm
tech.root: com
ms.assetid: 1bbffe63-bd3a-40c8-aece-63121a437269
ms.date: 12/05/2018
ms.keywords: GetClassObject, GetClassObject method [COM], GetClassObject method [COM],IClassActivator interface, IClassActivator interface [COM],GetClassObject method, IClassActivator.GetClassObject, IClassActivator::GetClassObject, _com_iclassactivator_getclassobject, com.iclassactivator_getclassobject, objidl/IClassActivator::GetClassObject
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IClassActivator::GetClassObject
 - objidl/IClassActivator::GetClassObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ObjIdl.h
 - CLUAMoniker
api_name:
 - IClassActivator.GetClassObject
---

# IClassActivator::GetClassObject


## -description

Retrieves a class object.

## -parameters

### -param rclsid [in]

The CLSID that identifies the class whose class object is to be retrieved.

### -param dwClassContext [in]

The context in which the class is expected to run. For a list of values, see the <a href="/windows/desktop/api/wtypesbase/ne-wtypesbase-clsctx">CLSCTX</a> enumeration.

### -param locale [in]

An LCID constant as defined in WinNls.h.

### -param riid [in]

The IID of the interface on the object to which a pointer is desired.

### -param ppv [out]

The address of pointer variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppv</i> contains the requested interface pointer.

## -returns

If the method succeeds, the return value is S_OK. Otherwise, it is E_FAIL.

## -see-also

<a href="/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject">CoGetClassObject</a>



<a href="/windows/desktop/api/objidl/nn-objidl-iclassactivator">IClassActivator</a>